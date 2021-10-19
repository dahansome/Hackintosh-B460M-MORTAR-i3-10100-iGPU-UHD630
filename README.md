# Hackintosh-MSI-B460M-MORTAR-i3-10100-iGPU-UHD630

## EFI

OpenCore: 0.7.4

Supports macOS11.2 ~ macOS12.0

## Hardware Configuration

| Configuration  | Model |
| ------------- | ------------- |
| CPU  | I3-10100  |
| CPU Cooler  | DEEPCOOL GAMMAXX400K  |
| Motherboard  |  MSI B460M MORTAR  |
| Memory |  ADATA DDR4 2666MHz 16G*1 | 
| Hard Disk | Kingston SSD SA400S37-240G |
| Graphics card  |  Intel UHD Graphics 630  |
| Monitor  |  SAMSUNG C24F390FHC 23.5"  1800R Free-sync HDMI |
| Power Supply  |  Segotep 600G 500W 80 Plus Gold |
| Wireless Card  |  FV-T919 BCM94360CD |

## What's Working/What's Not
### Working

- Onboard Audio (including digital audio)
- Bluetooth & Wi-Fi 
- Sleep/Wake
- HDMI -> HDMI
- DP -> HDMI
- App Store
- Power Nap
- NVRAM
### Not Working (as expected)

### Not Yet Tested
- Handoff
- AirPlay
- iMessage
- Facetime
- Ethernet
- All USB ports at 3.x speed

## CPU support
 - [x] Supports all 10-generation CPUs with UHD630 cores
 - [x] The 10th generation CPU of non-core display with F can also have the following independent display without drive (but cannot use nuclear display acceleration)
 
 ## Graphics card support
  - [x] Support UHD630 graphics card with only CPU core display
  - [x] Support AMD RX 470/480/570/570X/580/580X/590 series graphics cards
  - [x] Support AMD RX 5500/5600/5700 series graphics cards (dedicated config.plist required)
> PS: To use the independent display, you need to forcibly turn on the CPU core display in the BIOS (Advanced -> Built-in display configuration -> Integrated graphics multi-monitor (IGD Multi-monitor) -> Allow), otherwise the core display hardware decoding will fail and only use the core Obviously can be ignored


## BIOS settings
- USB device wake up from S3/S4/S5: Allow
- PS/2 mouse wake up from S3/S4/S5: Allow
- USB keyboard wake up from S3/S4/S5: any key
- Integrated graphics and multiple monitors: Allowed (otherwise the hardware decoding of the core display will fail, and those that only use the core display can be ignored)
- CFG lock: prohibited

## Onboard network card settings
System Preferences -> Network -> Ethernet (Advanced) -> Hardware -> Configuration: Manual, Speed: 100baseTX (1000baseT can be selected for Gigabit network environment), Duplex: Full Duplex, MTU: Standard 1500

