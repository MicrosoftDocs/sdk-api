---
UID: NS:ntddkbd._KEYBOARD_ATTRIBUTES
title: KEYBOARD_ATTRIBUTES (ntddkbd.h)
description: KEYBOARD_ATTRIBUTES specifies the attributes of a keyboard.
helpviewer_keywords: ["*PKEYBOARD_ATTRIBUTES","KEYBOARD_ATTRIBUTES","KEYBOARD_ATTRIBUTES structure [Human Input Devices]","PKEYBOARD_ATTRIBUTES","PKEYBOARD_ATTRIBUTES structure pointer [Human Input Devices]","hid.keyboard_attributes","kref_430bedf0-40bc-4d93-b382-3fe4c69fcbb5.xml","ntddkbd/KEYBOARD_ATTRIBUTES","ntddkbd/PKEYBOARD_ATTRIBUTES"]
old-location: hid\keyboard_attributes.htm
tech.root: hid
ms.assetid: 060e93de-b84e-4755-a5f8-cbc52d900310
ms.date: 12/05/2018
ms.keywords: '*PKEYBOARD_ATTRIBUTES, KEYBOARD_ATTRIBUTES, KEYBOARD_ATTRIBUTES structure [Human Input Devices], PKEYBOARD_ATTRIBUTES, PKEYBOARD_ATTRIBUTES structure pointer [Human Input Devices], hid.keyboard_attributes, kref_430bedf0-40bc-4d93-b382-3fe4c69fcbb5.xml, ntddkbd/KEYBOARD_ATTRIBUTES, ntddkbd/PKEYBOARD_ATTRIBUTES'
f1_keywords:
- ntddkbd/KEYBOARD_ATTRIBUTES
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ntddkbd.h
api_name:
- KEYBOARD_ATTRIBUTES
targetos: Windows
req.typenames: KEYBOARD_ATTRIBUTES, *PKEYBOARD_ATTRIBUTES
req.redist: 
ms.custom: 19H1
---

# KEYBOARD_ATTRIBUTES structure


## -description


KEYBOARD_ATTRIBUTES specifies the attributes of a keyboard.


## -struct-fields




### -field KeyboardIdentifier

Specifies the keyboard type and subtype in a KEYBOARD_ID structure:


```
typedef struct _KEYBOARD_ID {
  UCHAR  Type;
  UCHAR  Subtype;
} KEYBOARD_ID, *PKEYBOARD_ID;
```






#### Type

Specifies the keyboard type.



#### Subtype

Specifies the keyboard subtype, which is a vendor-specific value.



##### 


### -field KeyboardMode

Specifies the scan code mode. See the Remarks section.


### -field NumberOfFunctionKeys

Specifies the number of function keys that a keyboard supports.


### -field NumberOfIndicators

Specifies the number of LED indicators that a keyboard supports.


### -field NumberOfKeysTotal

Specifies the number of keys that a keyboard supports.


### -field InputDataQueueLength

Specifies the size, in bytes, of the input data queue used by the keyboard port driver.


### -field KeyRepeatMinimum

Specifies the minimum possible value for the keyboard typematic rate and delay in a <a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_typematic_parameters">KEYBOARD_TYPEMATIC_PARAMETERS</a> structure.


### -field KeyRepeatMaximum

Specifies the maximum possible value for the keyboard typematic rate and delay in a KEYBOARD_TYPEMATIC_PARAMETERS structure.


## -remarks



This structure is used with a <a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_attributes">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a> request to return information about the attributes that a keyboard supports.

For information about keyboard types, subtypes, scan code modes, and related keyboard layouts, see the documentation in *ntdd8042.h* and *ntddkbd.h* header in Windows SDK, and the [Keyboard Layout Samples](https://docs.microsoft.com/samples/microsoft/windows-driver-samples/keyboard-layout-samples/). 

Also see the [USB HID to PS/2 Scan Code Translation Table](http://download.microsoft.com/download/1/6/1/161ba512-40e2-4cc9-843a-923143f3456c/translate.pdf) specification from Microsoft.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_attributes">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>

<a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicators">IOCTL_KEYBOARD_QUERY_INDICATORS</a>

<a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicator_translation">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>

<a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_typematic">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>

<a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_set_indicators">IOCTL_KEYBOARD_SET_INDICATORS</a>

<a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_set_typematic">IOCTL_KEYBOARD_SET_TYPEMATIC</a>

<a href="https://docs.microsoft.com/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_typematic_parameters">KEYBOARD_TYPEMATIC_PARAMETERS</a>
