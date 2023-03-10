---
UID: NS:ntddkbd._KEYBOARD_ATTRIBUTES
title: KEYBOARD_ATTRIBUTES (ntddkbd.h)
description: KEYBOARD_ATTRIBUTES specifies the attributes of a keyboard.
helpviewer_keywords: ["*PKEYBOARD_ATTRIBUTES","KEYBOARD_ATTRIBUTES","KEYBOARD_ATTRIBUTES structure [Human Input Devices]","PKEYBOARD_ATTRIBUTES","PKEYBOARD_ATTRIBUTES structure pointer [Human Input Devices]","hid.keyboard_attributes","kref_430bedf0-40bc-4d93-b382-3fe4c69fcbb5.xml","ntddkbd/KEYBOARD_ATTRIBUTES","ntddkbd/PKEYBOARD_ATTRIBUTES"]
old-location: hid\keyboard_attributes.htm
tech.root: hid
ms.assetid: 060e93de-b84e-4755-a5f8-cbc52d900310
ms.date: 02/25/2021
ms.keywords: '*PKEYBOARD_ATTRIBUTES, KEYBOARD_ATTRIBUTES, KEYBOARD_ATTRIBUTES structure [Human Input Devices], PKEYBOARD_ATTRIBUTES, PKEYBOARD_ATTRIBUTES structure pointer [Human Input Devices], hid.keyboard_attributes, kref_430bedf0-40bc-4d93-b382-3fe4c69fcbb5.xml, ntddkbd/KEYBOARD_ATTRIBUTES, ntddkbd/PKEYBOARD_ATTRIBUTES'
req.header: ntddkbd.h
req.include-header: Ntddkbd.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: KEYBOARD_ATTRIBUTES, *PKEYBOARD_ATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KEYBOARD_ATTRIBUTES
 - ntddkbd/_KEYBOARD_ATTRIBUTES
 - PKEYBOARD_ATTRIBUTES
 - ntddkbd/PKEYBOARD_ATTRIBUTES
 - KEYBOARD_ATTRIBUTES
 - ntddkbd/KEYBOARD_ATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddkbd.h
api_name:
 - KEYBOARD_ATTRIBUTES
---

# KEYBOARD_ATTRIBUTES structure


## -description

Specifies the attributes of a keyboard.

## -struct-fields

### -field KeyboardIdentifier

Specifies the keyboard type and subtype in a KEYBOARD_ID structure:

```cpp
typedef struct _KEYBOARD_ID {
  UCHAR  Type;
  UCHAR  Subtype;
} KEYBOARD_ID, *PKEYBOARD_ID;
```

#### Type

Specifies the keyboard type.

| Value | Description                                          |
|:-----:|------------------------------------------------------|
|  0x4  | Enhanced 101- or 102-key keyboards (and compatibles) |
|  0x7  | Japanese Keyboard                                    |
|  0x8  | Korean Keyboard                                      |
| 0x51  | Unknown type or HID keyboard                         |

#### Subtype

Specifies the keyboard subtype, which is a vendor-specific value.

### -field KeyboardMode

Specifies the scan code mode. See the [Remarks](#remarks) section.

### -field NumberOfFunctionKeys

Specifies the number of function keys that a keyboard supports.

### -field NumberOfIndicators

Specifies the number of LED indicators that a keyboard supports.

### -field NumberOfKeysTotal

Specifies the number of keys that a keyboard supports.

### -field InputDataQueueLength

Specifies the size, in bytes, of the input data queue used by the keyboard port driver.

### -field KeyRepeatMinimum

Specifies the minimum possible value for the keyboard typematic rate and delay in a [KEYBOARD_TYPEMATIC_PARAMETERS](ns-ntddkbd-keyboard_typematic_parameters.md) structure.

### -field KeyRepeatMaximum

Specifies the maximum possible value for the keyboard typematic rate and delay in a [KEYBOARD_TYPEMATIC_PARAMETERS](ns-ntddkbd-keyboard_typematic_parameters.md) structure.

## -remarks

This structure is used with a [IOCTL_KEYBOARD_QUERY_ATTRIBUTES IOCTL](ni-ntddkbd-ioctl_keyboard_query_attributes.md) request to return information about the attributes that a keyboard supports.

For more information about keyboard types, subtypes, scan code modes, and related keyboard layouts, see [Keyboard and mouse HID client drivers](/windows-hardware/drivers/hid/keyboard-and-mouse-hid-client-drivers) in our drivers documentation.

More details can also be found in the *kbd.h*, *ntdd8042.h* and *ntddkbd.h* headers in the Windows SDK, the [USB HID to PS/2 Scan Code Translation Table](https://download.microsoft.com/download/1/6/1/161ba512-40e2-4cc9-843a-923143f3456c/translate.pdf) specification from Microsoft, and the [Keyboard Layout Samples](/samples/microsoft/windows-driver-samples/keyboard-layout-samples/).

## -see-also

[IOCTL_KEYBOARD_QUERY_ATTRIBUTES IOCTL](ni-ntddkbd-ioctl_keyboard_query_attributes.md)

[IOCTL_KEYBOARD_QUERY_INDICATORS IOCTL](ni-ntddkbd-ioctl_keyboard_query_indicators.md)

[IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION IOCTL](ni-ntddkbd-ioctl_keyboard_query_indicator_translation.md)

[IOCTL_KEYBOARD_QUERY_TYPEMATIC IOCTL](ni-ntddkbd-ioctl_keyboard_query_typematic.md)

[IOCTL_KEYBOARD_SET_INDICATORS IOCTL](ni-ntddkbd-ioctl_keyboard_set_indicators.md)

[IOCTL_KEYBOARD_SET_TYPEMATIC IOCTL](ni-ntddkbd-ioctl_keyboard_set_typematic.md)

[KEYBOARD_TYPEMATIC_PARAMETERS structure](ns-ntddkbd-keyboard_typematic_parameters.md)
