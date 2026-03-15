# Dungeon Explorer v1.0.6

A C# console-based dungeon-crawler game developed as part of a university Object-Oriented Programming (OOP) module assignment. The project demonstrates core OOP principles including inheritance, polymorphism, encapsulation, and interface-driven design.

## Objective

Survive and reach Room 7 without dying. Navigate through challenges including puzzles and monsters. Manage your inventory wisely — collect items and activate them to stay alive.

## Controls

Use the menu prompts displayed in the console to navigate. When you find an item, check your inventory and activate it from there.

## Log Files

After running the project, a `net9.0` folder will be generated. This folder contains test log files produced during gameplay.

## File Structure
```
Dungeon_Explorer/
├── DungeonExplorer/
│   ├── Classes/
│   │   ├── Creatures/
│   │   │   ├── Creature.cs        # Base creature class
│   │   │   ├── Monster.cs         # Monster subclass
│   │   │   ├── Player.cs          # Player subclass
│   │   │   ├── Envy.cs
│   │   │   ├── Gluttony.cs
│   │   │   ├── Greed.cs
│   │   │   ├── Lust.cs
│   │   │   ├── Pride.cs
│   │   │   ├── Sloth.cs
│   │   │   └── Wrath.cs
│   │   ├── Items/
│   │   │   ├── Item.cs            # Base item class
│   │   │   ├── Inventory.cs       # Inventory management
│   │   │   ├── Potion.cs
│   │   │   └── Weapon.cs
│   │   ├── Management/
│   │   │   ├── Fight.cs           # Combat logic
│   │   │   ├── GameTest.cs        # Test assertions
│   │   │   ├── Menu.cs            # UI menus
│   │   │   ├── Statistics.cs      # Player stats
│   │   │   └── Story.cs           # Room narratives
│   │   ├── Navigation/
│   │   │   ├── GameMap.cs         # Map and room tracking
│   │   │   └── Room.cs            # Room definition
│   │   └── Run/
│   │       ├── GameLoop.cs        # Main game loop
│   │       └── Program.cs         # Entry point
│   ├── Interfaces/
│   │   ├── ICollectible.cs
│   │   ├── IDamagable.cs
│   │   ├── IHealable.cs
│   │   ├── IHealthValidation.cs
│   │   └── IHelper.cs
│   ├── DungeonExplorer.csproj
│   └── README.md
├── .gitignore
└── DungeonExplorer.sln
```

## OOP Concepts Demonstrated

- **Inheritance** — `Monster` and `Player` extend `Creature`; `Potion` and `Weapon` extend `Item`
- **Polymorphism** — Sin-based monsters (e.g. `Envy`, `Wrath`) use dynamic polymorphism via the `Creature` hierarchy
- **Interfaces** — `IDamagable`, `IHealable`, `ICollectible`, `IHealthValidation`, `IHelper` define shared contracts
- **Encapsulation** — Game state is managed through dedicated classes (`GameMap`, `Inventory`, `Statistics`)

## Requirements

- .NET 9.0 SDK

## Running the Project
```bash
dotnet run --project DungeonExplorer/DungeonExplorer.csproj
```
