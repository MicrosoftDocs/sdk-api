---
UID: NS:winuser.TOUCHPAD_PARAMETERS
title: TOUCHPAD_PARAMETERS
description: Contains user touchpad settings, including system information related to all detected touchpads.
tech.root: winmsg
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

Contains user touchpad settings, including system information related to all detected touchpads.

## -struct-fields

### -field versionNumber

The version of the struct. Caller must set to TOUCHPAD_PARAMETERS_LATEST_VERSION to use the latest version, or to TOUCHPAD_PARAMETERS_VERSION_# to use a specific version. The version must be specified when both reading and writing settings.

### -field maxSupportedContacts^1^

The maximum number of simultaneous contacts (fingers) supported across all detected touchpads.

### -field legacyTouchpadFeatures^1^

The supported features reported by a legacy touchpad. This will be [LEGACY_TOUCHPAD_FEATURE_NONE](ne-winuser-legacy_touchpad_features.md) if no legacy touchpads are present, or if the legacy touchpad does not support configuration through the Serial Peripheral Interface (SPI).

### -field touchpadPresent^1^

A touchpad is detected.

### -field legacyTouchpadPresent^1^

A legacy touchpad is detected.

### -field externalMousePresent^1^

An external mouse is detected. See [Precision touchpad tuning](/windows-hardware/design/component-guidelines/touchpad-tuning-guidelines) for information on exempting a mouse from being considered as external (for the purposes of this status field).

### -field touchpadEnabled^1^

A touchpad is enabled.

### -field touchpadActive^1^

A touchpad is active. The touchpad is active if it is enabled, and either there is no external mouse detected or the touchpad has been configured to stay active despite the presence of an external mouse. This field does not indicate whether the touchpad is actively producing input.

### -field feedbackSupported^1^

A touchpad supports haptic feedback.

### -field clickForceSupported^1^

A touchpad supports haptic click force.

### -field Reserved1

### -field allowActiveWhenMousePresent^2^

A touchpad can remain active if an external mouse is detected. When inactive, any input produced by the touchpad is ignored.

### -field feedbackEnabled^2^

Haptic feedback is enabled on touchpads if supported.

### -field tapEnabled^2^

Single-finger taps are enabled.

### -field tapAndDragEnabled^2^

Tap-and-drag is enabled.

### -field twoFingerTapEnabled^2^

Two-finger tap is enabled.

### -field rightClickZoneEnabled^2^

Pressing the bottom-right corner of the touchpad results in a right-click instead of a left click.

If the user has swapped their left and right mouse buttons ([GetSystemMetrics(SM_SWAPBUTTON)](nf-winuser-getsystemmetrics.md) is true), the right-click zone is mirrored horizontally to the bottom-left corner of the touchpad.

### -field mouseAccelSettingHonored^2^

Mouse motion produced by the touchpad honors the user's mouse acceleration setting (specified by [SystemParametersInfo(SPI_GETMOUSE)](nf-winuser-systemparametersinfoa.md)). If false, the mouse motion always has acceleration applied.

### -field panEnabled^2^

Two-finger panning is enabled.

### -field zoomEnabled^2^

Two-finger zooming is enabled.

### -field scrollDirectionReversed^2^

The direction content scrolls with two-finger panning is reversed. By default, the upward motion of contacts on the touchpad results in content scrolling downward while leftward motion of contacts results in content scrolling rightwards.

### -field Reserved2

### -field sensitivityLevel^2^

The touchpad sensitivity level. The more sensitive the touchpad, the less suppression of mouse input generation occurs after keyboard activity (see [TOUCHPAD_SENSITIVITY_LEVEL enumeration](ne-winuser-touchpad_sensitivity_level.md)).

### -field cursorSpeed^2^

The rate at which the mouse motion produced by the touchpad moves the cursor. Valid values are 1-20, inclusive.

### -field feedbackIntensity^2^

The relative intensity of the touchpad's haptic feedback (if supported). Valid values are 0-100, inclusive.

### -field clickForceSensitivity^2^

The relative sensitivity of the touchpad's haptic click detection (if supported). Valid values are 0-100, inclusive.

### -field rightClickZoneWidth^2^

The relative width of the touchpad right-click zone. Valid values are 0-100, inclusive. If non-zero, this value overrides device configuration.

### -field rightClickZoneHeight^2^

The relative height of the touchpad right-click zone. Valid values are 0-100, inclusive. If non-zero, this value overrides device configuration.

## -remarks

All fields apply only to Precision Touchpads, with the exception of fields that specify "legacy touchpad" or are supported by the legacy touchpad as indicated by the *legacyTouchpadFeatures* field.

^1^Represents the system information that can be used to help inform which user settings are applicable to the current device. They are ignored when calling SystemParametersInfo ([A](nf-winuser-systemparametersinfoa.md)/[W](nf-winuser-systemparametersinfow.md)) with SPI_SETTOUCHPADPARAMETERS.

^2^Represents user settings. Modifications to these fields will result in changing the user's settings when calling SystemParametersInfo ([A](nf-winuser-systemparametersinfoa.md)/[W](nf-winuser-systemparametersinfow.md)) with SPI_SETTOUCHPADPARAMETERS.

## -see-also

[TOUCHPAD_SENSITIVITY_LEVEL enumeration](ne-winuser-touchpad_sensitivity_level.md), [LEGACY_TOUCHPAD_FEATURES enumeration](ne-winuser-legacy_touchpad_features.md)