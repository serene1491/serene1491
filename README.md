<div align="center">

# Hi! I'm Pop >.<

I build programming languages, runtimes, developer tools, and scripting platforms.

</div>

I primarily work with C#, Lua, Ruby on Rails, and a bit of Rust, developing projects involving native interoperability, source generation, secure scripting, language architecture, and distributed systems.

## Projects

### [PopLua](https://github.com/serene1491/PopLua) — Pop's Lua runtime

A Lua 5.4 runtime for C#, designed with a focus on:

* compile-time generated bindings;
* Native AOT compatibility;
* direct integration with the Lua C API;
* controlled and sandboxed execution;
* memory, time, and instruction limits;
* asynchronous APIs exposed to Lua;
* straightforward integration with .NET applications.

```csharp
[Module("level")]
public static partial class LevelsModule
{
    [Fn("start")]
    public static string Start(string name)
        => $"Starting level '{name}'";
}
```

### [Pop](https://github.com/poplanguage/pop) — Simple by nature. Powerful by design.

I contribute to the Pop programming language (yes, that’s my nickname), working on areas such as:

* standard library architecture;
* default visibility and return semantics;
* lazy sequences;
* MIR and LLVM backend execution;
* official extension packages;
* compilation and portability contracts;
* conformance testing.

```lua
namespace Game.Players

public record Player
    name: String
    score: Int = 0
end

public function award(player: Player, points: Int): Player
    return player with {
        score = player.score + points,
    }
end
```

### Macchi — More than configurable. Programmable.

A scripting platform composed of a C# Discord bot and a Ruby on Rails web application.

Its main areas include:

* secure Lua script execution;
* script publishing and versioning;
* centralized runtime limits;
* authentication and authorization;
* communication between execution hosts and the web platform.

Macchi uses PopLua as its shared scripting runtime.

```lua
-- The :docs entry point
function docs()
    macchi.reply("Open the Macchi Wiki for the Lua reference.")
end

-- The :status entry point
function status()
    next.secs(1) -- Simulate loading
    macchi.reply("Macchi is ready.")
end

message.new()
    :text("Choose an action.")
    :button("docs", "Docs")
    :button("status", "Status")
    :send()

-- A run() function is optional.
-- Top-level statements are executed normally.
```

## Areas of interest

* Programming language design
* Compilers and interpreters
* Runtimes and virtual machines
* Native Ahead-of-Time compilation
* Native interoperability
* Source generation
* Language Server Protocol
* Scripting APIs
* Sandboxing
* Distributed systems

## Technologies

<p>
  <img src="https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white" alt="C#" />
  <img src="https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white" alt=".NET" />
  <img src="https://img.shields.io/badge/Lua-2C2D72?style=flat-square&logo=lua&logoColor=white" alt="Lua" />

  <img src="https://img.shields.io/badge/Ruby-CC342D?style=flat-square&logo=ruby&logoColor=white" alt="Ruby" />
  <img src="https://img.shields.io/badge/Rails-D30001?style=flat-square&logo=rubyonrails&logoColor=white" alt="Ruby on Rails" />

  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/Git-181717?style=flat-square&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" />
</p>

## Currently in development

```text
PopLua
└── A modern Lua runtime for .NET applications
    github.com/serene1491/PopLua

Pop
└── A programming language, standard library, and developer toolchain
    github.com/poplanguage/pop

Macchi
└── More than configurable. Programmable.
    Currently private
```
