# MasqueGPS - Device Compatibility & Supported Devices

## Overview

MasqueGPS is a professional mock location tool designed for authorized QA testing, development, and diagnostics. This document outlines device compatibility, tested devices, and important disclaimers.

---

## Supported Android Versions

- **Minimum**: Android 7.0 (Nougat, API 24)
- **Recommended**: Android 10+ (best compatibility)

---

## Device Manufacturer Compatibility

### ✅ Fully Supported (Tested)

| Manufacturer | Status | Notes |
|--------------|--------|-------|
| **Xiaomi** | ✅ Fully tested | HyperOS, MIUI 12-15 verified |
| **Redmi** | ✅ Fully tested | Same as Xiaomi (HyperOS) |
| **POCO** | ✅ Fully tested | Same as Xiaomi (HyperOS) |

### ⚠️ Theoretically Supported (Not Yet Tested)

| Manufacturer | Status | Notes |
|--------------|--------|-------|
| **Google Pixel** | ⚠️ Should work | Stock Android, best theoretical compatibility |
| **OnePlus** | ⚠️ Should work | OxygenOS is close to stock Android |
| **Motorola** | ⚠️ Should work | Near-stock Android experience |
| **Nokia** | ⚠️ Should work | Android One program, near-stock |
| **Sony** | ⚠️ Should work | Xperia series, near-stock Android |

### ⚠️ Partially Supported (May Have Issues)

| Manufacturer | Status | Notes |
|--------------|--------|-------|
| **Samsung** | ⚠️ Untested, see disclaimer below | Knox security may interfere |
| **OPPO** | ⚠️ Untested | ColorOS has manufacturer-specific optimizations |
| **vivo** | ⚠️ Untested | FuntouchOS has manufacturer-specific optimizations |
| **Realme** | ⚠️ Untested | Realme UI is based on ColorOS |
| **ASUS** | ⚠️ Untested | ROG Phone/ZenFone, stock-like but untested |
| **Nothing** | ⚠️ Untested | Nothing OS is near-stock, should work |

### ❌ Not Supported

| Manufacturer | Status | Notes |
|--------------|--------|-------|
| **Huawei** | ❌ Not supported | No Google Mobile Services (GMS) |
| **Honor** | ⚠️ Depends | Newer models without GMS not supported |

---

## Chipset Compatibility

MasqueGPS works at the Android framework level and does **not** depend on specific chipsets:

- ✅ **Qualcomm Snapdragon** - Fully supported
- ✅ **MediaTek** - Should work (framework-level, not chipset-dependent)
- ✅ **Samsung Exynos** - Should work (framework-level)
- ✅ **Google Tensor** - Should work (framework-level)
- ✅ **Unisoc** - Should work (framework-level)

---

## Root vs Non-Root Compatibility

### Root Access (Recommended)
- **Stability**: Mock location is stable and persistent
- **Detection**: Best chance of avoiding detection
- **Limitations**: None significant
- **Requirements**: Rooted device with Magisk, KernelSU, or APatch

### Shizuku (Non-Root)
- **Stability**: Mock location may be corrected by real GPS within minutes
- **Detection**: Good, but less reliable than Root
- **Limitations**: Cannot disable hardware GPS
- **Requirements**: Shizuku app installed and authorized via ADB

---

## ⚠️ Samsung Devices - Important Disclaimer

### Samsung Knox Security

Samsung devices feature **Samsung Knox**, a hardware-based security platform that may interfere with mock location functionality.

**Important Points:**

1. **Knox Warranty Bit**: Samsung Knox includes a hardware fuse (warranty bit) that can be tripped by:
   - Rooting the device
   - Installing custom firmware
   - Modifying system partitions

2. **Knox Trip Consequences**:
   - **Warranty void**: Samsung may refuse warranty service
   - **Samsung Pay disabled**: May permanently disable Samsung Pay
   - **Secure Folder disabled**: May disable Samsung Secure Folder
   - **Samsung Health restrictions**: Some features may be limited
   - **Trade-in value reduced**: Device trade-in value may decrease

3. **MasqueGPS and Knox**:
   - MasqueGPS does **NOT** trip the Knox warranty bit
   - MasqueGPS does **NOT** modify system partitions
   - MasqueGPS does **NOT** require root on Samsung devices (Shizuku mode available)
   - However, if your device is **already rooted**, Knox may already be tripped

4. **User Responsibility**:
   - Users are responsible for understanding their device's Knox status
   - MasqueGPS developers are **NOT responsible** for any Knox-related issues
   - Users should verify their Knox status before using MasqueGPS on Samsung devices

### Samsung-Specific Limitations

- Samsung's location services may have additional mock location detection
- Samsung's "Improve Accuracy" settings may need to be manually disabled
- Some Samsung devices may require additional ADB permissions

### Recommendation for Samsung Users

1. **Check Knox status**: Dial `*#0*#` in the phone app, or use a Knox checker app
2. **If Knox is intact**: Use Shizuku mode (non-root) - safest approach
3. **If Knox is already tripped**: Root mode is available but understand the implications
4. **Test first**: Try the free version before purchasing

---

## Google Play Store Compatibility

- **Play Store version**: Android 10+ recommended
- **Play Protect**: May flag mock location apps - this is expected
- **Updates**: Keep MasqueGPS updated for latest compatibility fixes

---

## Testing Recommendations

Before purchasing MasqueGPS, please verify compatibility:

1. **Check Android version**: Must be Android 7.0+
2. **Check manufacturer**: Review the compatibility table above
3. **Check GMS**: Ensure Google Mobile Services are installed
4. **Test Shizuku**: Install Shizuku app and verify it works on your device
5. **Check Knox** (Samsung only): Verify your Knox status

---

## Known Incompatibilities

The following scenarios are **NOT supported**:

- Devices without Google Mobile Services (Huawei, some Chinese ROMs)
- Android versions below 7.0
- Emulators (detected and blocked)
- Devices with heavily modified custom ROMs (may work but untested)

---

## Disclaimer

MasqueGPS is provided "as-is" for authorized testing purposes. Users are responsible for:

- Understanding their device's security status (especially Knox on Samsung)
- Complying with applicable laws and terms of service
- Using MasqueGPS only on devices and apps they own or are authorized to test
- Any consequences of using mock location features

MasqueGPS developers are **NOT responsible** for:
- Device warranty issues
- Knox-related problems on Samsung devices
- Detection by third-party apps
- Any misuse of the application

---

## Support

For device-specific issues, please provide:
- Device manufacturer and model
- Android version
- Root status (Rooted/Shizuku/Neither)
- Knox status (Samsung only)
- Detailed description of the issue

---

*Last updated: June 11, 2026*
