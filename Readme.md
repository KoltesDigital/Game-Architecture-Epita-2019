# Game Architecture - EPITA 2019

> Course materials. Contains voluntary errors and design flaws which are addressed during the courses :)

## Requirements

Although the code should support multiple platforms, only precompiled libraries for Windows are given.

1. [Visual Studio 2017](https://www.visualstudio.com/downloads/)
2. [Premake 5](https://premake.github.io/download.html)

## Build

### Windows

    premake5.exe vs2017

Open _build\StealthFactor.sln_, choose your target, and build.

### Linux

    apt-get install -y g++ g++-multilib libode-dev libsfml-dev make
    premake5 gmake2
    cd build
    make config=release_linux64

## External dependencies

1. [cli.cpp](https://github.com/KoltesDigital/cli.cpp), a CLI argument parser (header-only)
2. [ODE](http://www.ode.org/), a physics engine
3. [pugixml](http://pugixml.org/), an XML parser (header-only)
4. [SFML](https://www.sfml-dev.org/), a small multimedia framework

## Session #1

- Architecture principle: rely on lower level, cannot access to higher level.
- Overview of a typical game engine architecture.

## Session #2

- Dependency cycles to be avoided.
- Singletons can facilitate architecture breaches.
- Division of responsibilities.
- Interfaces to break dependency cycles.
- Dependency injection.
- Dependency inversion.
- pImpl.
- void\*: C-style pointer to user data.

## Session #3

- RAII.
- Ownership.
- std::unique_ptr.
- std::shared_ptr.
- Move semantics.
- Interface with opaque structures through handlers.

## Session #4

- Specialization through inheritance.
- Specialization through components, entity-component-system.
- Camera system.
- Separation between Model and View.
- Visitor pattern.

## Session #5

- Serialization.
- Visitor pattern, again.
- Unit tests.
- Model-View, again.
- Command pattern.
- Advanced Command: Undo-Redo.
- Metrics.
