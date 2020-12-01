---
UID: NS:ntddkbd._KEYBOARD_INDICATOR_TRANSLATION
title: KEYBOARD_INDICATOR_TRANSLATION (ntddkbd.h)
description: KEYBOARD_INDICATOR_TRANSLATION specifies a device-specific, variable length array of mappings between keyboard scan codes and LED indicators.
helpviewer_keywords: ["*PKEYBOARD_INDICATOR_TRANSLATION","KEYBOARD_INDICATOR_TRANSLATION","KEYBOARD_INDICATOR_TRANSLATION structure [Human Input Devices]","PKEYBOARD_INDICATOR_TRANSLATION","PKEYBOARD_INDICATOR_TRANSLATION structure pointer [Human Input Devices]","hid.keyboard_indicator_translation","kref_937bedf9-89bf-4db8-ad4d-2e8354a163f6.xml","ntddkbd/KEYBOARD_INDICATOR_TRANSLATION","ntddkbd/PKEYBOARD_INDICATOR_TRANSLATION"]
old-location: hid\keyboard_indicator_translation.htm
tech.root: hid
ms.assetid: 7ee6ab87-b8fa-4d2c-a51f-5a20ed836d6a
ms.date: 12/05/2018
ms.keywords: '*PKEYBOARD_INDICATOR_TRANSLATION, KEYBOARD_INDICATOR_TRANSLATION, KEYBOARD_INDICATOR_TRANSLATION structure [Human Input Devices], PKEYBOARD_INDICATOR_TRANSLATION, PKEYBOARD_INDICATOR_TRANSLATION structure pointer [Human Input Devices], hid.keyboard_indicator_translation, kref_937bedf9-89bf-4db8-ad4d-2e8354a163f6.xml, ntddkbd/KEYBOARD_INDICATOR_TRANSLATION, ntddkbd/PKEYBOARD_INDICATOR_TRANSLATION'
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
req.typenames: KEYBOARD_INDICATOR_TRANSLATION, *PKEYBOARD_INDICATOR_TRANSLATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KEYBOARD_INDICATOR_TRANSLATION
 - ntddkbd/_KEYBOARD_INDICATOR_TRANSLATION
 - PKEYBOARD_INDICATOR_TRANSLATION
 - ntddkbd/PKEYBOARD_INDICATOR_TRANSLATION
 - KEYBOARD_INDICATOR_TRANSLATION
 - ntddkbd/KEYBOARD_INDICATOR_TRANSLATION
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
 - KEYBOARD_INDICATOR_TRANSLATION
---

# KEYBOARD_INDICATOR_TRANSLATION structure


## -description

KEYBOARD_INDICATOR_TRANSLATION specifies a device-specific, variable length array of mappings between keyboard scan codes and LED indicators.

## -struct-fields

### -field NumberOfIndicatorKeys

Specifies the number of elements in the <b>IndicatorList</b> array.

### -field IndicatorList

Specifies a device-specific, variable-length array of INDICATOR_LIST structures.


```
typedef struct _INDICATOR_LIST {
  USHORT  MakeCode;
  USHORT  IndicatorFlags;
} INDICATOR_LIST, *PINDICATOR_LIST;
```






#### MakeCode

Specifies the make scan code that is generated when a key is pressed.



#### IndicatorFlags

Specifies the LED indicator that corresponds to the <b>MakeCode</b> scan code. For information about the flags, see the <b>LedFlags</b> member of the <a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_parameters">KEYBOARD_INDICATOR_PARAMETERS</a> structure.

## -remarks

This structure is used with an <a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicator_translation">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a> request to obtain indicator translation information.

## -see-also

<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_attributes">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicators">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicator_translation">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_typematic">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_set_indicators">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_set_typematic">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_indicator_parameters">KEYBOARD_INDICATOR_PARAMETERS</a>