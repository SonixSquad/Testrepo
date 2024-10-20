# Testrepo

Last Updated 05/05/25 Patch Notes below..

This is intended as a base build to start from with the following systems ready:

UE [5.3 C++] Project with BaseCharacter classes in C++ [totw_baseCharacter] derived from [GSCModularPlayerStateCharacter]
GAS implemented with ASC on PlayerState for Player Characters using [GasCompanion]
Default [GSCAttributeSet] [Health, MaxHealth, Mana, MaxMana, Stamina, MaxStamina]
First Person Character [GunFaction] with test trace shooting ability
Third Person Character [MeleeFaction] with test melee hit ability
Basic widget menu on beginPlay to select which Faction character to spawn as [key TAB] to show menu and then [shift+F1] to focus mouse cursor.
AI with HealthBar widget (displayed OnHit) and ASC on Character and with C++ Parent [totw_baseAI_Character] derived from [GSCModularCharacter] and using [GSCAIController]
HTN [MovetoRandomLocation] and other tasks
Ability to spawn bots via keybind [key 3]
2 seperated zones on 1 map for testing different aspects of gameplay as GunFaction or MeleeFaction Character.
Resizable GreyBox structure for map layout design [materials nabbed from Lyra].
Disabled [HotReload] and [LiveCoding] UE functions for better compatibility with Rider IDE workflow.
The required used plugin list is as follows:

GAS Companion
Darker Nodes
Electronic Nodes
HTN Planning
Additional plugins enabled but not yet used (disable in Build.cs if not available or required for new project):

SKGShooterFramework
Terminal Ballistics
Combat Components
//------------------------------------ PATCH NOTES //-------------------------------------

v1.0.0.4

Shooting and damage now work
Beginning of coop lobby implementation (use keys 1 to host, 2 to Join lobby on packaged build) //------------------------------------- v1.0.0.3
Initial integration of SKG Framework
Characters now have weps equipped on spawn.
Each character has their own Animgraph //------------------------------------- v1.0.0.2
Basic Melee Attack combo now works, intended to be built upon.
Adjusted background of menu screen to not be clickable anymore (cursor would lose focus)
Known Issues - upcoming changes

Stamina/Mana/HP Regen implemented but not working currently
Multiplayer not yet implemented, currently single player only.
Substepping for melee not yet implemented, simple Sphere trace currently
Actual melee / Gun Weapon spawn logic not yet implemented
Linked Animation Graph per faction not yet implemented //-------------------------------------
v1.0.0.1

Now using 1 single character BP that loads in factional variables upon class selection (mesh / IMC / AbilitySet)
SLightly nicer Menu, bigger buttons
Spawn logic changed, now sending spawned character to the custom spawn pad rather than possessing existing character in level.
