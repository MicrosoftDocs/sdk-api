---
UID: NS:winuser.TOUCHPAD_PARAMETERS
title: TOUCHPAD_PARAMETERS
description: Contains user touchpad settings and system information related to all detected touchpads.
tech.root: InputMsg
ms.date: 03/27/2024
ms.keywords: '*TOUCHPAD_PARAMETERS, TOUCHPAD_PARAMETERS, TOUCHPAD_PARAMETERS structure pointer, TOUCHPAD_PARAMETERS, TOUCHPAD_PARAMETERS structure, tagTOUCHPAD_PARAMETERS, winuser/TOUCHPAD_PARAMETERS'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 11, version 24H2 [desktop apps only]
req.target-min-winversvr: None supported
prerelease: true
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
targetos: Windows
req.typenames: TOUCHPAD_PARAMETERS, *PTOUCH_PAD_PARAMETERS, TOUCHPAD_PARAMETERS_V1, *PTOUCHPAD_PARAMETERS_V1
ms.custom: 24H2
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - TOUCHPAD_PARAMETERS
 - PTOUCH_PAD_PARAMETERS
f1_keywords:
 - TOUCHPAD_PARAMETERS
 - winuser/TOUCHPAD_PARAMETERS
 - PTOUCH_PAD_PARAMETERS
 - winuser/PTOUCH_PAD_PARAMETERS
dev_langs:
 - c++
helpviewer_keywords:
 - TOUCHPAD_PARAMETERS
---

# TOUCHPAD_PARAMETERS structure

## -description

Contains user touchpad settings and system information related to all detected touchpads.

> [!NOTE]
> The term "touchpad" refers to Precision Touchpads. The term "legacy touchpad" refers to older generation touchpads that report themselves to Windows as a mouse.

## -struct-fields

### -field versionNumber

The version of the struct.

Caller must set to TOUCHPAD_PARAMETERS_LATEST_VERSION to use the latest version, or to TOUCHPAD_PARAMETERS_VERSION_[#] to use a specific version (). The version must be specified when both reading and writing settings.

> [!NOTE]
> TOUCHPAD_PARAMETERS_VERSION_1 is the only specific version of TOUCHPAD_PARAMETERS_VERSION_[#] currently defined.

### -field maxSupportedContacts

The maximum number of simultaneous contacts (for the touchpad that supports the most) amongst all detected touchpads.<sup>1</sup>

### -field legacyTouchpadFeatures

The supported features reported by detected legacy touchpads. This will be [LEGACY_TOUCHPAD_FEATURE_NONE](ne-winuser-legacy_touchpad_features.md) if no legacy touchpads are detected, or if the legacy touchpads do not support configuration through *SPI_SETTOUCHPADPARAMETERS*.<sup>1</sup>

### -field touchpadPresent

A Precision Touchpad is detected.<sup>1</sup>

### -field legacyTouchpadPresent

A legacy touchpad is detected.<sup>1</sup>

### -field externalMousePresent

An external mouse is detected. See [Precision touchpad tuning](/windows-hardware/design/component-guidelines/touchpad-tuning-guidelines) for information on exempting a mouse from being considered as external (for the purposes of this status field and behavior of the *allowActiveWhenMousePresent* setting).<sup>1</sup>

### -field touchpadEnabled

Touchpad input is enabled.<sup>1</sup>

### -field touchpadActive

Touchpad input is active. It is active if it is enabled, and either there is no external mouse detected or touchpad input has been configured to stay active despite the presence of an external mouse. This field does not indicate whether any touchpad is actively producing input.<sup>1</sup>

### -field feedbackSupported

A detected touchpad supports haptic feedback.<sup>1</sup>

### -field clickForceSupported

A detected touchpad supports haptic click force.<sup>1</sup>

### -field Reserved1

### -field allowActiveWhenMousePresent

Touchpad input can remain active if an external mouse is detected. When inactive, any input produced by a touchpad is ignored.<sup>2</sup>

### -field feedbackEnabled

Haptic feedback is enabled on touchpads if supported.<sup>2</sup>

### -field tapEnabled

Single-finger taps are enabled.<sup>2</sup>

### -field tapAndDragEnabled

Tap-and-drag is enabled.<sup>2</sup>

### -field twoFingerTapEnabled

Two-finger tap is enabled.<sup>2</sup>

### -field rightClickZoneEnabled

Pressing the bottom-right corner of the touchpad results in a right-click instead of a left click.<sup>2</sup>

If the user has swapped their left and right mouse buttons ([GetSystemMetrics(SM_SWAPBUTTON)](nf-winuser-getsystemmetrics.md) is true), the right-click zone is mirrored horizontally to the bottom-left corner of the touchpad.

### -field mouseAccelSettingHonored

Mouse motion produced by the touchpad honors the user's mouse acceleration setting (specified by [SystemParametersInfo(SPI_GETMOUSE)](nf-winuser-systemparametersinfoa.md)). If false, the mouse motion always has acceleration applied.<sup>2</sup>

### -field panEnabled

Two-finger panning is enabled.<sup>2</sup>

### -field zoomEnabled

Two-finger zooming is enabled.<sup>2</sup>

### -field scrollDirectionReversed

The direction content scrolls with two-finger panning is reversed. By default, the upward motion of contacts on the touchpad results in content scrolling downward while leftward motion of contacts results in content scrolling rightwards.<sup>2</sup>

### -field Reserved2

### -field sensitivityLevel

The touchpad sensitivity level. The more sensitive the touchpad, the less suppression of mouse input generation occurs after keyboard activity (see [TOUCHPAD_SENSITIVITY_LEVEL enumeration](ne-winuser-touchpad_sensitivity_level.md)).<sup>2</sup>

### -field cursorSpeed

The rate at which the mouse motion produced by the touchpad moves the cursor. Valid values are 1-20, inclusive.<sup>2</sup>

### -field feedbackIntensity

The relative intensity of the touchpad's haptic feedback (if supported). Valid values are 0-100, inclusive.<sup>2</sup>

### -field clickForceSensitivity

The relative sensitivity of the touchpad's haptic click detection (if supported). Valid values are 0-100, inclusive.<sup>2</sup>

### -field rightClickZoneWidth

The relative width of the touchpad right-click zone. Valid values are 0-100, inclusive. If non-zero, this value overrides the device configuration.<sup>2</sup>

### -field rightClickZoneHeight

The relative height of the touchpad right-click zone. Valid values are 0-100, inclusive. If non-zero, this value overrides the device configuration.<sup>2</sup>

## -remarks

All fields apply only to Precision Touchpads, with the exception of fields that specify "legacy touchpad" or are supported by the legacy touchpad as indicated by the *legacyTouchpadFeatures* field.

<sup>1</sup> Represents the system information that can be used to help inform which user settings are applicable to the current device. They are ignored when calling SystemParametersInfo ([A](nf-winuser-systemparametersinfoa.md)/[W](nf-winuser-systemparametersinfow.md)) with SPI_SETTOUCHPADPARAMETERS.

<sup>2</sup> Represents user settings. Modifications to these fields will result in changing the user's settings when calling SystemParametersInfo ([A](nf-winuser-systemparametersinfoa.md)/[W](nf-winuser-systemparametersinfow.md)) with SPI_SETTOUCHPADPARAMETERS.

## -see-also

[TOUCHPAD_SENSITIVITY_LEVEL enumeration](ne-winuser-touchpad_sensitivity_level.md), [LEGACY_TOUCHPAD_FEATURES enumeration](ne-winuser-legacy_touchpad_features.md)