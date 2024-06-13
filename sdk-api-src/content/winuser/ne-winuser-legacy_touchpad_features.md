---
UID: NE:winuser.LEGACY_TOUCHPAD_FEATURES
tech.root: InputMsg
title: LEGACY_TOUCHPAD_FEATURES
ms.date: 03/27/2024
targetos: Windows
description: Identifies the settings for which a legacy touchpad has indicated support.
prerelease: true
req.construct-type: enumeration
req.ddi-compliance: 
req.header: winuser.h
req.include-header: Windows.h
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11, version 24H2 [desktop apps only]
req.target-min-winversvr: None supported
req.target-type: Windows
req.typenames: LEGACY_TOUCHPAD_FEATURES
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - LEGACY_TOUCHPAD_FEATURES
f1_keywords:
 - LEGACY_TOUCHPAD_FEATURES
 - winuser/LEGACY_TOUCHPAD_FEATURES
dev_langs:
 - c++
helpviewer_keywords:
 - LEGACY_TOUCHPAD_FEATURES
---

# LEGACY_TOUCHPAD_FEATURES enumeration

## -description

Identifies the settings for which a legacy touchpad has indicated support.

## -enum-fields

### -field LEGACY_TOUCHPAD_FEATURE_NONE:0x00000000

No touchpad features are supported (or no legacy touchpad is detected).

### -field LEGACY_TOUCHPAD_FEATURE_ENABLE_DISABLE:0x00000001

The legacy touchpad supports being enabled and disabled.

### -field LEGACY_TOUCHPAD_FEATURE_REVERSE_SCROLL_DIRECTION:0x00000004

The legacy touchpad supports reversing its scroll direction.

## -remarks

When the corresponding setting is updated with SPIF_UPDATEINIFILE (to persist the setting), the legacy touchpad will respond accordingly.

## -see-also

[TOUCHPAD_PARAMETERS structure](ns-winuser-touchpad_parameters.md)
