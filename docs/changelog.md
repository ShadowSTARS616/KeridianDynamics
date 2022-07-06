# Changelog  
  
| modName    | Keridian Dynamics (KDVA)                                          |
| ---------- | ----------------------------------------------------------------- |
| license    | CC-BY-SA-4.0                                                      |
| author     | Eleusis La Arwall and zer0Kerbal                                  |
| forum      | (https://forum.kerbalspaceprogram.com/index.php?/topic/202945-*/) |
| github     | (https://github.com/zer0Kerbal/zer0Kerbal/KeridianDynamics)       |
| curseforge | (https://www.curseforge.com/kerbal/ksp-mods/KeridianDynamics)     |
| spacedock  | (https://spacedock.info/mod/308)                                  |
| ckan       | KeridianDynamicsVesselAssembly                                    |

## Version 0.8.99.0-prerelease - `<Please Read the Instructions #1>` edition

* 04 Jul 2022
* Released for Kerbal Space Program 1.12.x

### Changes

This is the first in a series of updates to this addon. Each update will update some of the parts and patches so that instead of one massive update, I can update the addon in a more manageable way.

* Parts Updated in this Pass:
  * [KDChemicalReactor]
  * [KD3DPrinter-250.cfg]
  * [KD-SledgeHammer.cfg]
  * Cargo Tanks
    * [KD-ST1001FS]
    * [KD-ST1251FS]
    * [KD-ST1252FS]
    * [KD-ST1253FS]

### minor changes

* [SimpleConstruction.cfg] v v1.1.0.0
  * add header
  * remove `!` hitchhiker
    * was
      * @MODULE[ModuleResourceConverter],*:HAS[!#ConverterName[Ore-->Metal+LFO]]
    * now
      * @MODULE[ModuleResourceConverter],*:HAS[#ConverterName[Ore-->Metal+LFO]]
* [KD-OSERocketParts.cfg] v1.1.0.0
  * PatchManager\PluginData
  * add header
  * was
    * @OSE_DefaultRecipe:AFTER[Workshop]
  * now
    * @OSE_DefaultRecipe:NEEDS[Workshop]:AFTER[Workshop]
  * was
    * @PART[*]:HAS[OSE_PartRecipe:HAS[#MaterialKits[1]]]:AFTER[Workshop]
  * now
    * @PART[*]:HAS[@OSE_PartRecipe:HAS[#MaterialKits[1]]]:NEEDS[Workshop]:AFTER[Workshop]+

### Compatibility

* [KerbalInventorySystem.cfg] v1.1.0.0
  * rename from [KIS.cfg]
  * remove Sledgehammer patches
  * no longer necessary

### Parts

* Replace
  * [KD-3DPrinter.cfg] NEW
  * [KD-3D-Printer.cfg] Original
  * new part name is: KD-3DPrinter-250
* [ghostparts.cfg]
  * which will go away with version 0.9.0.0-release
    * KD-3D-Printer
    * KD-3DPrinter
* Update/Lint/Asset pass
  * [KD-ST1001FS] v1.1.0.0
  * [KD-ST1251FS] v1.1.0.0
  * [KD-ST1252FS] v1.1.0.0
  * [KD-ST1253FS] v1.1.0.0
  * [KD-SledgeHammer.cfg] v1.1.0.0
    * move KIS module into part
    * add :NEEDS[KIS] to make part only show if KIS is installed
  * closes #6 - [Bug 🐞]: Also survey stakes are upside down when placed,
  * closes #5 - [Bug 🐞]: Cannot equip sledgehammer or stakes
  
### Graphical changes

* Resize Flags
  * from 256x160 to 512x320
* HeroLogo
  * update

### IVA/Spaces

* renamed from `_` to `-` in IVA names
* started splitting out the individual IVA's into separate files

### Localization

* Add
  * [readme.md] v2.1.2.0
  * [quickstart.md] v1.0.1.1
* Many minor updates to [en-us.cfg]
  * including renaming from us-en.cfg to en-us.cfg
  * simplified the localization string names
  * scraped KSP dictionary for settings
* [KS-FAVA.cfg]
  * [@ShadowSTAR616](https://github.com/ShadowSTARS616) reports
  * part now localized
  * closes #37 - [Bug 🐞]: KS-FAVA part not localized
* [KDChemicalReactor]
  * add "2.5m" to title
* [KD3DPrinter-250.cfg]
  * add "2.5m" add "2.5m" to title
* updates #33 - Part Localization
* updates #16 - English <us-en.cfg>
* updates #15 - Localization - Master

### Status

* Issues
  * closes #10 - KeridianDynamics 0.8.99.0-prerelease `<Please Read the Instructions #1>` edition
  * closes #11 - 0.8.99.0-prerelease Verify Legal Mumbo Jumbo
  * closes #12 - 0.8.99.0-prerelease Update Documentation
  * closes #13 - 0.8.99.0-prerelease Social Media
  * closes #4 - friznit updates

---

## Version 0.8.9.1-prerelease - `<Brushing off the Construction Dust>`

* >>-- adopted for curation by @zer0Kerbal --<<
* moved changelog into separate file
* Changelog.md -> Kerbal Changelog Changelog.cfg
* updated Readme.md
* created Forum Thread
* updated SpaceDock
* renamed GitHub repository to NotSoSimpleConstruction
* updated CKAN/NetKAN
* modernization, polish, update pass on .cfg
* large .png -> .dds
* added .version file
* added license(s) file(s)
* merged in patches
* automated deploy/release process

// much lint was shaved
// misplaces spare right brace in Changelog.cfg
// Changelog.cfg:32 :: unexpected }
// KD-ExtensionPad.cfg:224 :: unexpected }
// KD-Keronica.cfg:164 :: unexpected }
// KD-LaunchPad.cfg:132 :: unexpected }
// KD-LaunchPadSide.cfg:138 :: unexpected }
// KD-LaunchPadTop.cfg:138 :: unexpected }
// KD-Pad.cfg:84 :: unexpected }

---

## Version 0.8.9.1 - `<Vacuuming the Carpets>`

* initial update to 1.7.3
* updated KIS (thank you to Justin @Khalendros)

 ---

## Version 0.8.9(.0) - The No-Title-Pre-Release Update

* 2018.04.15
* Compatibility to EL 6.0
* Re-export all models (except Internals)
  * unity 2017.1.3p1
  * latest parttools
* B9PartSwitch support
* A Resource-Switcher (FS, IFS or B9PS) is now mandatory
* All Resource Converters are enabled by default (some require CRP)
* Patchmanager support
* Ore->Metal converters can be disabled
* MetalOre->Metal converters can be disabled
* ScrapMetal->Metal converters can be disabled
* Metal->RocketParts converters can be disabled
* Metal->MaterialKits converters can be disabled
* Metal+Ore->SpecializedParts converters can be disabled
* Dirt->RareMetals+ExoticMinerals converters can be disabled
* Old costs can be restored
* Station Tank Series can be disabled
* (Cargo) Tank Series can be disabled
* Station Tank Series can be crewed
* OSE Workshop default Resource can be switched from MaterialKits to RocketParts
* Integrated 534443s cost-rebalance (thanks a lot!)
* Reintegrated Station Tank Series
* Fixed unused switcher for Cargo Tanks
* StockDrill Patch only applies if no other MetalOre harvester is present already
* Added MetalOre Harvester to MiniDrill
* Reworked Spawn Markers
* Redo MetalOre converters (density change 0.0275->0.026)
* Removed very old hexagonal tanks used when FS and IFS are not installed (no replacement)
* Removed KD-OrbitalPad, KD-SidePad and KD-TopPad
* New Parts:
  * KD-Keronica
    * Rework of the old OrbitalPad
    * Advanced Probe Core with Launchpad.
  * KD-LaunchPad
    * 2 Variants 1.25, 2.5
    * Light-weight replacement for OrbitalPad
  * KD-LaunchPadSide
    * 2 Variants 1.25, 2.5
    * Light-weight replacement for SidePad
  * KD-LaunchPadTop
    * 2 Variants 1.25, 2.5
    * Light-weight replacement for TopPad
  * KD-ExtensionPad
  * 6 variants, 0.625-5.0 meters
  * Light-weight part to extend exisiting vessels (ELDisposablePad)
  * KD-FAVA (early prototype)
    * Fully Automated Vessel Assembler
    * generates productivity without the need for Kerbals

### Localization

* English

 ---

## Version 0.8.2(.0) - Recycling Everything

* 2017.01.21
* Moved parts to customisation: KD-STXXXXFS. New Adapters included.
* New part
  * KD-FurnaceSmall
  * KD-FabricationContainer
    * Metal --> Rocketparts
    * needs an engineer
  * KD-PAM
    * Planetary Assembly Management aka SurveyStation
    * has no IVA currently
  * KD-PAMSmall.
  * KD-RecyclerSmall
  * KD-RecycleSite
    * Needs KAS
  * KD-T125XFS (X=variant)
    * 1.25 m Storage Tanks
    * 3 sizes(1, 2, 4 m)).
  * KD-T2001FS
    * 1.25 to 2.5 m storage adapter
* Re-exported most of the models with improved shading and materials.
* Re-worked most of the animations. Except the tanks all parts use ModuleColorChange for glow animations (can be changed in cfg).
* Overhauled resource storage and mass for ALL tanks.
* Added
  * ScrapMetal setup
  * LFO setup (temporary, for balancing. Will be replaced in the future).
  * surface attach to some parts (Launchpads for example).
* Fixed Furnaces MetalOre extraction ratio. Now really 70% (was 100 before).
* Recycling produces ScrapMetal and small amounts of Metal.
* Added
  * ScrapMetal-->Metal converters
  * Furnaces
  * ChemicalReactor
* Changed SpecialistBonus
  * KD-Furnace
  * KD-3D-Printer
* ChemicalReactor can now extract RareMetals and ExoticMinerals from Dirt (if OSE Workshop is installed).
* Changed dependency for Metal,
  * Ore-->SpecializedParts converter to require UmbraSpaceIndustries.
* Changed SimpleConstruction support:
  * If SC is installed the following changes are applied:
    1. No MetalOre Harvester.
    2. No MetalOre-->Metal converters.
    3. Ore-->Metal converters give 70 times more Metal.
    4. Metal tanks storage-capacity is increased by factor 5 (ingame units, not mass!).
* Changed FS/IFS priority
  * If both are installed IFS module will be used.
* Added optional config to use RocketParts with OSE Workshop instead of MaterialKits, RareMetals & ExoticMinerals (KeridianDynamics-OSE-RP.cfg).

 ---

## Version 0.8.1(.0) - Balancing update one

* 2016-11-28
* New part
  * KD-ChemicalReactor
    * Ore --> Metal+LFO
  * KD-T250XFS (X=variant)
    * 2.5 m non-passable Storage Tanks
    * 3 sizes (1, 2, 3 m).
  * KD-T375XFS (X=variant)
    * 3.75 m non-passable Storage Tanks
    * 3 sizes (1, 3, 6 m).
  * KD-T3252FS
    * 3.75 m to 2.5 m non-passable Storage Tank adapter (2 m).
* Removed parts
  * KD-T125FS
  * KD-T250FS
* Increased
  * Furnace conversion speed
  * ~15 times faster, extr.-rate remains 1%-mass
* Added
  * MetalOre --> Metal converter to Furnace by default (~70%-mass extr.-rate).
  * MetalOre harvester to Stock drill (Big one only).
* Increased
  * 3D-Printer conversion speed
  * ~21 times faster, conv.-rate remains 100%-mass
* Reduced
  * 3D-Printer mass to 1.85 tons
* Compatibility patch
  * SimpleConstruction.
* Updated converter specialty
  * ExperienceEffect
    * 3D Printer and Furnace = ConverterSkill
    * ChemicalReactor = ScienceSkill
* Added
  * [bulkheadProfiles]
  * [tags]
  * ScienceExperiment
    * OreScience to Stock Drill
    * Big one only

 ---

## Version 0.8(.0.0) - Storage update

* 2016-07-06
* New part
  * KD-OrbitalHangar
    * Big Launchpad for orbital construction and other stuff.
  * KD-ST250XFS (X=variant)
    * 2.5 m crew-passable Storage Tanks
    * 3 sizes (1, 2, 3 m).
  * KD-ST375XFS (X=variant)
    * 3.75 m crew-passable Storage Tanks
    * 3 sizes (1, 3, 6 m).
  * KD-ST3252FS
    * 3.75 m to 2.5 m crew-passable Storage Tank adapter (2 m).
* Community Resource Pack now triggers storage configurations for MaterialKits,... (instead of OSE because CRP is bundled with OSE).
* Added
  * JSI Advanced Transparant Pods dependency
  * ConnectedLivingSpace support.
  * optional config that allows the 3D-Printer to make MaterialKits from Metal in customisation.
* KD-MobileVAB
  * Minor model tweaks
  * Airlock moved to the bottom
  * Fixed IVA light.
* LaunchSite
  * One arm glows in a darker blue now.
* Launchpads and MobileVAB have proper names for EL GUI.
* All parts
  * rebalanced in cost
  * cost to unlock
  * tech-node (Stock and CTT).
* Changed capacity for MaterialKits, RareMetals, ExoticMinerals and Monoprop. on old tanks.

 ---

## Version 0.7(.0.0) - Universal Assembly

* 2016-05-16
* New Parts
  * KD-MobileVAB
    * Acts primary as Survey Station
    * offers a high productivity factor for up to 12 Kerbals.
  * New part (previously experimental)
    * KD-LaunchSite (reworked)
      * Acts as Survey Stake.
    * KD-SledgeHammer
      * Needed to attach the LaunchSite to the ground.
  * All parts above need Kerbal Inventory System to work properly.
* Added support for OSE workshop.
* KD-3D-Printer can convert Ore to MaterialKits.
* KD-MobileVAB can be used as OSE workshop and OSE recycler.
* KD-T125FS and KD-T250FS have 2 additional setups
  * Materialkits
  * RareMetals/ExoticMinerals
* InterstellarFuelSwitch
  * is not a dependency anymore
  * still supported and highly recommended.
* Added support
  * Firespitter
    * FSmeshSwitch
    * FSfuelSwitch
* Added
  * MM-config
  * autodetects if Firespitter and/or InterstellarFuelSwitch is installed and applies the corresponding modules to the tanks. (If both are NOT installed, two tanks for RocketParts and two tanks for Metal are available)

 ---

## Version 0.6.1(.0) - PECUNIA PER KERBULUS

* 2016-05-01
* Reexported models
  * Unity 5
  * PartTools 1.1.
* New Company Motto
  * PECUNIA PER KERBULUS
  * Thanks to DaniDE for translation!
* Reworked Logo and Flags.
* Used "Icon_Hidden" tag
  * Thanks to Badsector for the hint!
* Added ExperimentalSection
  * needs KIS
* New experimental part
  * KD-Fundament
    * Thanks to colmo for the suggestion!
  * KD-LaunchSite
  * KD-SledgeHammer "Susie"

 ---

## Version 0.6(.0.0) - Recycling

* 2016-04-16
* Added Interstellar Fuel Switch dependency.
  * Tank names have changed, be careful with savegames!
* Reworked models
  * Colliders have not changed.
* Added Normal maps.
* Added Emissive maps.
* Added new animations.
* Reworked Furnace behavior
  * No more seperate heating needed.
* Furnace needs much less EC but produces more heat.
* New part
  * KD-Recycler
  * Roll-animation and ExRecycler need to be activated seperately
* Updated CTT-compatibility.

 ---

## Version 0.5(.0.0) - 2016 update

* 2016-02-27
* Reworked tanks. (Names have changed, so be carefull with savegames!)
* Changed RoverPads to TopPad and SidePad. (Names have changed, so be carefull with savegames!)
* New mesh-colliders for all parts (be carefull with savegames!).
* Toggleable Spawn Marker for all Pads added. A vessel from SPH will point in the direction of the arrowtip. VAB vessels will still point upwards.
* tanks now share the same texture
  * KD-OrbitalPad
  * KD-SidePad
  * KD-TopPad
  * all KD-OrbitalPad.dds
* Added thermal properties to KD-Pad and KD-OrbitalPad to prevent overheating-explosions during vessel-launch (might be exploitable ...).
* Added thermal curves to KD-Furnace and KD-3D-Printer.
* The Furnace needs to heat up before Metal can be extracted. CoreTemperature must at least reach 1800 K to start the extraction! Heating needs a lot of ElectricCharge. Once the extraction has started the heater can be turned off.
* The 3D-Printer needs 20 ElectricCharge instead of 10. It needs RoomTemperature to operate (300 K). Heat production is rather low.
* Some minor model and texture changes.
* Added 512x512 textures to Customisation.
* Added "KD-Example Craft.craft" to Customisation.
* Updated CTT-compatibility.

 ---

## Version 0.4(.0.0) - License update

* 2015-08-23
* License changed to CC-BY-SA 4.0 International
* New experimental parts
  * KD-RoverPad
  * KD-RoverPad2
* KD-Furnace
  * CoM -0.1 down
* KD-Pad
  * CoM -0.87 down
* KD-OrbitalPad
  * CoM -0.47 down
* Moved MM-patches for EL into one config. (Delete old versions before updating!)

 ---

## Version 0.3(.0.0) - Orbital Assembly

* 2015-08-10
* New part
  * KD-OrbitalPad
* KD-Pad fixes
  * Now transparent in Editor when not attached.
* Model and texture refined.
* Center of mass adjusted.
* KD-3D-Printer
  * Model and texture refined (a little).
* Added support for AVC.

 ---

## Version 0.2(.0.0) - Hotfix

* 2015-08-03
* Fixed MM-config for MetalOreFurnace and MetallicOreFurnace.
* Reconverted textures to DDS.

 ---

## Version 0.1(.0.0) - Initial Release

* 2015-07-27
* New part: KD-Furnace
* New part: KD-3D-Printer
* New part: KD-Pad
* New part: KD-TankHex1-Metal
* New part: KD-TankHex1-RocketParts
* New part: KD-TankHex2-Metal
* New part: KD-TankHex2-RocketParts

---