---
UID: NS:winuser.TOUCHPAD_PARAMETERS
tech.root: winmsg
title: TOUCHPAD_PARAMETERS
ms.date: 03/27/2024
targetos: Windows
description: Contains user touchpad settings, including system information related to all detected touchpads.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winuser.h
req.include-header: Windows.h
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 11, version 24H2 [desktop apps only]
req.target-min-winversvr: None supported
req.target-type: Windows
req.typenames: TOUCHPAD_PARAMETERS, *PTOUCH_PAD_PARAMETERS, TOUCHPAD_PARAMETERS_V1, *PTOUCHPAD_PARAMETERS_V1
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

Contains user touchpad settings, including system information related to all detected touchpads.

## -struct-fields

### -field versionNumber

The version of the struct. Caller must set to TOUCHPAD_PARAMETERS_LATEST_VERSION to use the latest version, or to TOUCHPAD_PARAMETERS_VERSION_# to use a specific version. The version must be specified when both reading and writing settings.

### -field maxSupportedContacts<sup>1</sup>

The maximum number of simultaneous contacts (fingers) supported across all detected touchpads.

### -field legacyTouchpadFeatures<sup>1</sup>

The supported features reported by a legacy touchpad. This will be [LEGACY_TOUCHPAD_FEATURE_NONE](ne-winuser-legacy_touchpad_features.md) if no legacy touchpads are present, or if the legacy touchpad does not support configuration through this Serial Peripheral Interface (SPI).

### -field touchpadPresent<sup>1</sup>

A touchpad is detected.

### -field legacyTouchpadPresent<sup>1</sup>

A legacy touchpad is detected.

### -field externalMousePresent<sup>1</sup>

An external mouse is detected. See [Precision touchpad tuning](/windows-hardware/design/component-guidelines/touchpad-tuning-guidelines) for information on exempting a mouse from being considered as external (for the purposes of this status field).

### -field touchpadEnabled<sup>1</sup>

A touchpad is enabled.

### -field touchpadActive<sup>1</sup>

A touchpad is active. The touchpad is active if it is enabled, and either there is no external mouse detected or the touchpad has been configured to stay active despite the presence of an external mouse. This field does not indicate whether the touchpad is actively producing input.

### -field feedbackSupported<sup>1</sup>

A touchpad supports haptic feedback.

### -field clickForceSupported<sup>1</sup>

A touchpad supports haptic click force.

### -field Reserved1

### -field allowActiveWhenMousePresent<sup>2</sup>

A touchpad can remain active if an external mouse is detected. When inactive, any input produced by the touchpad is ignored.

### -field feedbackEnabled<sup>2</sup>

Haptic feedback is enabled on touchpads if supported.

### -field tapEnabled<sup>2</sup>

Single-finger taps are enabled.

### -field tapAndDragEnabled<sup>2</sup>

Tap-and-drag is enabled.

### -field twoFingerTapEnabled<sup>2</sup>

Two-finger tap is enabled.

### -field rightClickZoneEnabled<sup>2</sup>

Pressing the bottom-right corner of the touchpad results in a right-click instead of a left click.

If the user has swapped their left and right mouse buttons ([GetSystemMetrics(SM_SWAPBUTTON)](nf-winuser-getsystemmetrics.md) is true), the right-click zone is mirrored horizontally to the bottom-left corner of the touchpad.

### -field mouseAccelSettingHonored<sup>2</sup>

Mouse motion produced by the touchpad honors the user's mouse acceleration setting (specified by [SystemParametersInfo(SPI_GETMOUSE)](nf-winuser-systemparametersinfoa.md)). If false, the mouse motion always has acceleration applied.

### -field panEnabled<sup>2</sup>

Two-finger panning is enabled.

### -field zoomEnabled<sup>2</sup>

Two-finger zooming is enabled.

### -field scrollDirectionReversed<sup>2</sup>

The direction content scrolls with two-finger panning is reversed. By default, the upward motion of contacts on the touchpad results in content scrolling downward while leftward motion of contacts results in content scrolling rightwards.

### -field Reserved2

### -field sensitivityLevel<sup>2</sup>

The touchpad sensitivity level. The more sensitive the touchpad, the less suppression of mouse input generation occurs after keyboard activity (see [TOUCHPAD_SENSITIVITY_LEVEL enumeration](ne-winuser-touchpad_sensitivity_level.md)).

### -field cursorSpeed<sup>2</sup>

The rate at which the mouse motion produced by the touchpad moves the cursor. Valid values are 1-20, inclusive.

### -field feedbackIntensity<sup>2</sup>

The relative intensity of the touchpad's haptic feedback (if supported). Valid values are 0-100, inclusive.

### -field clickForceSensitivity<sup>2</sup>

The relative sensitivity of the touchpad's haptic click detection (if supported). Valid values are 0-100, inclusive.

### -field rightClickZoneWidth<sup>2</sup>

The relative width of the touchpad right-click zone. Valid values are 0-100, inclusive. If non-zero, this value overrides device configuration.

### -field rightClickZoneHeight<sup>2</sup>

The relative height of the touchpad right-click zone. Valid values are 0-100, inclusive. If non-zero, this value overrides device configuration.

## -remarks

All fields apply only to Precision Touchpads, with the exception of fields that specify "legacy touchpad" or are supported by the legacy touchpad as indicated by the *legacyTouchpadFeatures* field.

<sup>1</sup>Represents the system information that can be used to help inform which user settings are applicable to the current device. They are ignored when calling SystemParametersInfo ([A](nf-winuser-systemparametersinfoa.md)/[W](nf-winuser-systemparametersinfow.md)) with SPI_SETTOUCHPADPARAMETERS.

<sup>2</sup>Represents user settings. Modifications to these fields will result in changing the user's settings when calling SystemParametersInfo ([A](nf-winuser-systemparametersinfoa.md)/[W](nf-winuser-systemparametersinfow.md)) with SPI_SETTOUCHPADPARAMETERS.

## -see-also

[TOUCHPAD_SENSITIVITY_LEVEL enumeration](ne-winuser-touchpad_sensitivity_level.md), [LEGACY_TOUCHPAD_FEATURES enumeration](ne-winuser-legacy_touchpad_features.md)