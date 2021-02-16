---
UID: NS:ntddkbd._KEYBOARD_EXTENDED_ATTRIBUTES
title: KEYBOARD_EXTENDED_ATTRIBUTES (ntddkbd.h)
description: KEYBOARD_EXTENDED_ATTRIBUTES specifies the extended attributes of a keyboard.
helpviewer_keywords: ["*PKEYBOARD_EXTENDED_ATTRIBUTES","KEYBOARD_EXTENDED_ATTRIBUTES","KEYBOARD_EXTENDED_ATTRIBUTES structure [Human Input Devices]","PKEYBOARD_EXTENDED_ATTRIBUTES","PKEYBOARD_EXTENDED_ATTRIBUTES structure pointer [Human Input Devices]","hid.keyboard_extended_attributes","ntddkbd/KEYBOARD_EXTENDED_ATTRIBUTES","ntddkbd/PKEYBOARD_EXTENDED_ATTRIBUTES"]
tech.root: hid
ms.assetid: 8320d76f-bef6-4a0f-afef-721d4b288481
ms.date: 08/06/2020
ms.keywords: '*PKEYBOARD_EXTENDED_ATTRIBUTES, KEYBOARD_EXTENDED_ATTRIBUTES, KEYBOARD_EXTENDED_ATTRIBUTES structure [Human Input Devices], PKEYBOARD_EXTENDED_ATTRIBUTES, PKEYBOARD_EXTENDED_ATTRIBUTES structure pointer [Human Input Devices], hid.KEYBOARD_EXTENDED_ATTRIBUTES, ntddkbd/KEYBOARD_EXTENDED_ATTRIBUTES, ntddkbd/PKEYBOARD_EXTENDED_ATTRIBUTES'
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
req.typenames: KEYBOARD_EXTENDED_ATTRIBUTES, *PKEYBOARD_EXTENDED_ATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KEYBOARD_EXTENDED_ATTRIBUTES
 - ntddkbd/_KEYBOARD_EXTENDED_ATTRIBUTES
 - PKEYBOARD_EXTENDED_ATTRIBUTES
 - ntddkbd/PKEYBOARD_EXTENDED_ATTRIBUTES
 - KEYBOARD_EXTENDED_ATTRIBUTES
 - ntddkbd/KEYBOARD_EXTENDED_ATTRIBUTES
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
 - KEYBOARD_EXTENDED_ATTRIBUTES
---

# KEYBOARD_EXTENDED_ATTRIBUTES structure


## -description

KEYBOARD_EXTENDED_ATTRIBUTES specifies the extended attributes of a keyboard.

## -struct-fields

### -field Version

Type: **UCHAR**

The version of this structure.

Only **KEYBOARD_EXTENDED_ATTRIBUTES_STRUCT_VERSION_1** supported.

### -field FormFactor

Type: **UCHAR**

Keyboard Form Factor (Usage ID: *0x2C1*).

| Value | Description                                              |
|-------|----------------------------------------------------------|
| 0x00  | Unknown Form Factor.                                     |
| 0x01  | Full‐Size keyboard.                                      |
| 0x02  | Compact keyboard. Such keyboards are less than 13” wide. |

### -field KeyType

Type: **UCHAR**

Keyboard Key Type (Usage ID: *0x2C2*).

| Value | Description                                        |
|-------|----------------------------------------------------|
| 0x00  | Unknown Key Type.                                  |
| 0x01  | Full‐travel keys.                                  |
| 0x02  | Low‐travel keys such as those on laptop keyboards. |
| 0x03  | Zero‐travel or virtual keys.                       |

### -field PhysicalLayout

Type: **UCHAR**

Keyboard Physical Layout (Usage ID: *0x2C3*).

| Value | Description                                                                              |
|-------|------------------------------------------------------------------------------------------|
| 0x00  | Unknown Layout                                                                           |
| 0x01  | 101 (e.g., US)                                                                           |
| 0x02  | 103 (Korea)                                                                              |
| 0x03  | 102 (e.g., German)                                                                       |
| 0x04  | 104 (e.g., ABNT Brazil)                                                                  |
| 0x05  | 106 (DOS/V Japan)                                                                        |
| 0x06  | Vendor‐specific – If specified, **VendorSpecificPhysicalLayout** must also be specified. |

This value does not refer to the legend set printed on the keys, but only to the physical keyset layout, defined by the relative location and shape of the textual keys in relation to each other. This value indicates which of the de facto standard physical layouts to which the keyboard conforms. These layouts are commonly understood.

### -field VendorSpecificPhysicalLayout

Type: **UCHAR**

A numeric identifier of the particular Vendor‐specific Keyboard Physical Layout (Usage ID: *0x2C4*).

Values for this field are defined by the hardware vendor but 0x00 is defined to not specify a Vendor‐specific Keyboard Physical Layout. If non‐zero, **PhysicalLayout** must have value *0x06*. If this identifier is *0x00*, **PhysicalLayout** must not have the value 0x06.

### -field IETFLanguageTagIndex

Type: **UCHAR**

String index of a String Descriptor having an IETF Language Tag (Usage ID: 0x2C5).

Actual string can be obtained via [IOCTL_HID_GET_INDEXED_STRING](/windows-hardware/drivers/ddi/hidclass/ni-hidclass-ioctl_hid_get_indexed_string) IOCTL in kernel-mode drivers or [HidD_GetIndexedString](/windows-hardware/drivers/ddi/hidsdi/nf-hidsdi-hidd_getindexedstring) call in user-mode applications.

This Language Tag specifies the intended primary locale of the keyboard legend set, conformant to [IETF BCP 47](https://www.rfc-editor.org/rfc/bcp/bcp47.txt) or its successor.

If an appropriate IETF Language Tag is not available, such as for custom, adaptive or new layouts, the value is set to 0x00.

### -field ImplementedInputAssistControls

Type: **UCHAR**

Bitmap for physically implemented input assist controls. (Usage ID: *0x2C6*).

| Bit   | Description                                        |
|-------|----------------------------------------------------|
| All 0 | No Keyboard Input Assist controls are implemented. |
| Bit 0 | Previous Suggestion                                |
| Bit 1 | Next Suggestion                                    |
| Bit 2 | Previous Suggestion Group                          |
| Bit 3 | Next Suggestion Group                              |
| Bit 4 | Accept Suggestion                                  |
| Bit 5 | Cancel Suggestion                                  |
|       | All other bits reserved.                           |

## -remarks

This structure is used with a [IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES](ni-ntddkbd-ioctl_keyboard_query_extended_attributes.md) request to return information about the extended attributes that a keyboard supports.

This information comes from HID Keyboard Report Descriptor described in [HID Usage Table Review Request 42: Consumer Page Keyboard Assist Controls](https://www.usb.org/sites/default/files/hutrr42c_0.pdf).

## -see-also

[IOCTL_KEYBOARD_QUERY_EXTENDED_ATTRIBUTES](ni-ntddkbd-ioctl_keyboard_query_extended_attributes.md)

[IOCTL_KEYBOARD_QUERY_ATTRIBUTES](ni-ntddkbd-ioctl_keyboard_query_attributes.md)

[HID Usage Table Review Request 42: Consumer Page Keyboard Assist Controls](https://www.usb.org/sites/default/files/hutrr42c_0.pdf)