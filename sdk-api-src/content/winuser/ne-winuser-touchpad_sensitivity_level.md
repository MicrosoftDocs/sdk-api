---
UID: NE:winuser.TOUCHPAD_SENSITIVITY_LEVEL
tech.root: InputMsg
title: TOUCHPAD_SENSITIVITY_LEVEL
ms.date: 03/27/2024
targetos: Windows
description: Identifies values for the touchpad sensitivity settings.
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
req.typenames: TOUCHPAD_SENSITIVITY_LEVEL
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - TOUCHPAD_SENSITIVITY_LEVEL
f1_keywords:
 - TOUCHPAD_SENSITIVITY_LEVEL
 - winuser/TOUCHPAD_SENSITIVITY_LEVEL
dev_langs:
 - c++
helpviewer_keywords:
 - TOUCHPAD_SENSITIVITY_LEVEL
---

# TOUCHPAD_SENSITIVITY_LEVEL enumeration

## -description

Identifies values for the touchpad sensitivity setting.

## -enum-fields

### -field TOUCHPAD_SENSITIVITY_LEVEL_MOST_SENSITIVE:0x00000000

The touchpad does not suppress mouse input generation after keyboard activity.

### -field TOUCHPAD_SENSITIVITY_LEVEL_HIGH_SENSITIVITY:0x00000001

The touchpad applies less mouse input suppression after keyboard activity.

### -field TOUCHPAD_SENSITIVITY_LEVEL_MEDIUM_SENSITIVITY:0x00000002

The touchpad applies its default level of mouse input suppression after keyboard activity.

### -field TOUCHPAD_SENSITIVITY_LEVEL_LOW_SENSITIVITY:0x00000003

The touchpad applies more mouse input suppression after keyboard activity.

### -field TOUCHPAD_SENSITIVITY_LEVEL_LEAST_SENSITIVE:0x00000004

The touchpad applies its maximum amount of mouse input suppression after keyboard activity.

## -remarks

The touchpad sensitivity setting causes the touchpad to suppress generation of mouse input after the user has typed on their keyboard. A higher sensitivity means the touchpad is more sensitive to touchpad input and does not suppress mouse input generation as much after keyboard activity.

## -see-also

