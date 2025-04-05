# KELFBinder: UMCS Installer
![Total Downloads:](https://img.shields.io/github/downloads/NathanNeurotic/KELFbinder-UMCS/total?color=blue&label=Total%20Downloads%3A&style=plastic)

**Forked from KELFBinder by [El_isra](https://israpps.github.io/) and modified by [NathanNeurotic](https://github.com/NathanNeurotic)**

Unified Memory Card System (UMCS) is a structural standard created by [TnA-Plastic](https://github.com/TnA-Plastic), consolidating exploits and updates into a unified setup. [Learn more](https://www.psx-place.com/forums/ps2-application-system.279/).

## Included Applications & Modules:
- **OPEN PS2 LOADER - MMCE** - https://github.com/ps2-mmce/Open-PS2-Loader/releases
- **BOOT.ELF**: [PS2BBL-MMCE](https://israpps.github.io/PlayStation2-Basic-BootLoader/) by [israpps](https://github.com/israpps)
- **BOOT2.ELF**: [wLaunchELF EXFAT-MMCE](https://israpps.github.io/projects/wlaunchelf-isr) by [israpps](https://github.com/israpps) (Hold `Start` during boot for emergency access)
- **OSDMENU.ELF**: [PS2BBL-OSDMENU](https://github.com/pcm720/PlayStation2-Basic-BootLoader) linked to [OSDMENU](https://github.com/pcm720/osdmenu-launcher) by [pcm720](https://github.com/pcm720)
- **launcher.elf & patcher.elf**: [OSDMENU Launcher & Loader](https://github.com/pcm720/osdmenu-launcher) by [pcm720](https://github.com/pcm720)
- **neutrino**: [Neutrino](https://github.com/rickgaiser/neutrino) by [rickgaiser](https://github.com/rickgaiser)
- **POPSTARTER exFAT USB Drivers**: [BDM Assault](https://github.com/israpps/BDMAssault) by [israpps](https://github.com/israpps)
- **POPSTARTER SMB Modules**: [SMB POPSTARTER](https://bitbucket.org/ShaolinAssassin/popstarter-documentation-stuff/wiki/quickstart-smb) by [ShaolinAssassin](https://github.com/ShaolinAssassin)
- **DKWDRV**: [GitHub Repository](https://github.com/DKWDRV/DKWDRV)
- **ESR Launcher** (Manual Launch): by [HowlingWolfHWC](https://github.com/HowlingWolfHWC)
- **FMCB Versions and Umbrella**:
  - Power Off ELF ([FreeMcBoot](https://israpps.github.io/FreeMcBoot-Installer/))
  - FMCB 1.953 Decrypted ([FreeMcBoot](https://israpps.github.io/FreeMcBoot-Installer/))
  - FMCB 1.966 Decrypted ([FreeMcBoot](https://israpps.github.io/FreeMcBoot-Installer/))
  - FMCB Configurator ([FreeMcBoot Configurator](https://israpps.github.io/FreeMcBoot-Installer/))
- **SAS-Compliant Installation** ([PS2Wiki](https://ps2wiki.github.io/sas-apps-archive/))
- **Custom Icon modifications**: by [koraxial](https://github.com/koraxial), [NathanNeurotic](https://github.com/NathanNeurotic)

### UMCS Required Directories:
- **SYS-CONF**: Contains universal configurations for many applications and exploits.
- **BOOT**: Contains the heart of UMCS, contains essential ELFs and their local settings.
- **B?EXEC-SYSTEM**: PS2BBL Exploit relevant to your console(s) region(s).
- **FMCBD-1.??**, or **OSDMENU**: At least one of the three available boots to land on. Otherwise you will only have the option to hold start to access wLaucnhELF.

## Configuration & Boot Order:
By default, the boot sequence searches in this order:

1. **FMCB 1.966** *(Recommended for most users)*  
   - If working, you may safely delete FMCB 1.953, RESTART, and POWEROFF.

2. **FMCB 1.953** *(Fallback if 1.966 fails due to modchips or hardware incompatibilities)*
   - If 1.966 fails, delete it to automatically revert to 1.953.

3. **OSDMENU** *(Alternative launcher if both FMCB versions fail)*
   - If both FMCB versions are incompatible, delete them and FMCB Configurator,  to activate OSDMENU automatically.

### Emergency Access:
If all three primary boot options fail:
- Hold `Start` during boot to launch **wLaunchELF_EXFAT-MMCE** (BOOT2.ELF).
- Modify launch order or applications via:
  - `mc?:/SYS-CONF/PS2BBL.INI`
  - `mc?:/BOOT/CONFIG.INI`
  - `mc?:/SYS-CONF/PSXBBL.INI`
- Alternative launchers (e.g., `mass:/XEB+/XEBPLUS.ELF`) can be configured to launch using wLaunchELF's built-in text editor.

### Additional Notes:
- Applications are accessible if installed; however, removing unused applications via the PS2 Browser (Memory Card Icon Screen) is recommended to free space.
- Customize boot preferences by editing `mc?:/SYS-CONF/PS2BBL.INI`.
- PSX consoles (PSX-DESR) default to launching wLaunchELF (configured via `PSXBBL.INI`).
- OSDMENU settings (`OSDMENU.CNF`) can be customized via wLaunchELF's text editor.

### Compatibility with Late PS2 Slim Models:
For late-model slim consoles incompatible with standard exploits, install any update even though it will say incompatible, and then launch the included OpenTuna Icon Installer to gain access to UMCS via OpenTuna.
![KELFBinder  _ _KELFBinder_20250404074959](https://github.com/user-attachments/assets/c6e7378a-9913-4e88-993d-da43f68835d4)

# 📂 HOW TO INSTALL – SIMPLE INSTRUCTIONS (USB ONLY)

Welcome! Follow these steps carefully to install UMCS to your memory card using a USB drive.  
---

## ✅ WHAT YOU'LL NEED:

- One **USB flash drive**

Your USB must meet these requirements:

- **FAT32** or **exFAT** format  
- **MBR (Master Boot Record)** partition table  
- **Cluster size: 32KB or 64KB**

💡 Need help formatting your USB drive properly? Use [rufus.ie](https://rufus.ie) — it's simple and free.

---

## 📥 STEP-BY-STEP INSTRUCTIONS

### 1. Prepare the USB Drive

- Insert your **USB drive** into your computer.
- Find the folder named:

```
KELFbinder-UMCS
```

- Copy the **entire folder** (as-is) to the **root of your USB drive**.

Do not rename or move files inside the folder. Do not remove any files or folders.

---

## ✅ Your USB should look something like this:

```
KELFbinder-UMCS/
├── FULL_CHANGELOG.TXT
├── KELFbinder.elf
├── KELFbinder_debug_udpbd.elf
├── LICENSE.TXT
├── README.md
├── common/
├── INSTALL/
├── lang/
```

---

## 🧩 FINAL STEP – INSTALL UMCS

1. Plug the **USB drive** into your PS2.
2. Launch **uLaunchELF**/**wLaunchELF**).
3. Navigate to:
```
mass:/KELFbinder-UMCS/
```
4. Run:
```
KELFbinder.elf
```
5. Follow on-screen instructions to complete installation.

---

## ❌ DON’T DO THIS:

- ❌ Don’t move files out of the folder.
- ❌ Don’t rename anything.

---

## 💡 NEED HELP?

Reread the steps, or ask the community — we’re here to help!

---------------------------------------------------------------------
ORIGINAL README:
---------------------------------------------------------------------
DVDPlayer and System Updates Manager for SCE PlayStation2

![GitHub all releases](https://img.shields.io/github/downloads/israpps/KELFBinder/total)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/8e886d46292e4d558c1c35a3387bffd5)](https://app.codacy.com/gh/israpps/KELFBinder/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade)

[![](https://img.shields.io/badge/Read%20the-Documentation-0020ff?style=for-the-badge&logo=pencil&labelColor=yellow)](https://israpps.github.io/KELFBinder/)
