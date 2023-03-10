---
UID: NS:ntddkbd._KEYBOARD_TYPEMATIC_PARAMETERS
title: KEYBOARD_TYPEMATIC_PARAMETERS (ntddkbd.h)
description: KEYBOARD_TYPEMATIC_PARAMETERS specifies a keyboard's typematic settings.
helpviewer_keywords: ["*PKEYBOARD_TYPEMATIC_PARAMETERS","KEYBOARD_TYPEMATIC_PARAMETERS","KEYBOARD_TYPEMATIC_PARAMETERS structure [Human Input Devices]","PKEYBOARD_TYPEMATIC_PARAMETERS","PKEYBOARD_TYPEMATIC_PARAMETERS structure pointer [Human Input Devices]","hid.keyboard_typematic_parameters","kref_1ef2a956-3ef3-40fc-be6e-4ce8c97f2e52.xml","ntddkbd/KEYBOARD_TYPEMATIC_PARAMETERS","ntddkbd/PKEYBOARD_TYPEMATIC_PARAMETERS"]
old-location: hid\keyboard_typematic_parameters.htm
tech.root: hid
ms.assetid: 4bbf1699-1ba9-4569-97ac-156a91405586
ms.date: 12/05/2018
ms.keywords: '*PKEYBOARD_TYPEMATIC_PARAMETERS, KEYBOARD_TYPEMATIC_PARAMETERS, KEYBOARD_TYPEMATIC_PARAMETERS structure [Human Input Devices], PKEYBOARD_TYPEMATIC_PARAMETERS, PKEYBOARD_TYPEMATIC_PARAMETERS structure pointer [Human Input Devices], hid.keyboard_typematic_parameters, kref_1ef2a956-3ef3-40fc-be6e-4ce8c97f2e52.xml, ntddkbd/KEYBOARD_TYPEMATIC_PARAMETERS, ntddkbd/PKEYBOARD_TYPEMATIC_PARAMETERS'
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
req.typenames: KEYBOARD_TYPEMATIC_PARAMETERS, *PKEYBOARD_TYPEMATIC_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KEYBOARD_TYPEMATIC_PARAMETERS
 - ntddkbd/_KEYBOARD_TYPEMATIC_PARAMETERS
 - PKEYBOARD_TYPEMATIC_PARAMETERS
 - ntddkbd/PKEYBOARD_TYPEMATIC_PARAMETERS
 - KEYBOARD_TYPEMATIC_PARAMETERS
 - ntddkbd/KEYBOARD_TYPEMATIC_PARAMETERS
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
 - KEYBOARD_TYPEMATIC_PARAMETERS
---

# KEYBOARD_TYPEMATIC_PARAMETERS structure


## -description

KEYBOARD_TYPEMATIC_PARAMETERS specifies a keyboard's typematic settings.

## -struct-fields

### -field UnitId

Specifies the unit number of a keyboard device. A keyboard device name has the format \Device\KeyboardPort<i>N</i>, where the suffix <i>N </i> is the unit number of the device. For example, a device, whose name is \Device\KeyboardPort0, has a unit number of zero, and a device, whose name is \Device\KeyboardPort1, has a unit number of one.

### -field Rate

Specifies the rate at which character output from a keyboard repeats, in characters per second, after a key is pressed and continuously held down. The minimum possible value is KEYBOARD_TYPEMATIC_RATE_MINIMUM and the maximum possible value is KEYBOARD_TYPEMATIC_RATE_MAXIMUM. The default value is KEYBOARD_TYPEMATIC_RATE_DEFAULT.

### -field Delay

Specifies the amount of time that must elapse, in milliseconds, after a key is pressed and continuously held down, before the character output from a keyboard begins to repeat. The minimum possible delay is KEYBOARD_TYPEMATIC_DELAY_MINIMUM and the maximum possible delay is KEYBOARD_TYPEMATIC_DELAY_MAXIMUM. The default value is KEYBOARD_TYPEMATIC_DELAY_DEFAULT.

## -remarks

This structure is used with <a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_typematic">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a> and <a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_set_typematic">IOCTL_KEYBOARD_SET_TYPEMATIC</a> requests to query and set a keyboard's typematic settings.

## -see-also

<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_attributes">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicators">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicator_translation">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_typematic">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_set_indicators">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_set_typematic">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="/windows/desktop/api/ntddkbd/ns-ntddkbd-keyboard_unit_id_parameter">KEYBOARD_UNIT_ID_PARAMETER</a>