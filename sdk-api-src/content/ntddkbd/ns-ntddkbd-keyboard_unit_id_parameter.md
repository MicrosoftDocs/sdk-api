---
UID: NS:ntddkbd._KEYBOARD_UNIT_ID_PARAMETER
title: KEYBOARD_UNIT_ID_PARAMETER (ntddkbd.h)
description: KEYBOARD_UNIT_ID_PARAMETER specifies the unit ID that Kbdclass assigns to a keyboard.
helpviewer_keywords: ["*PKEYBOARD_UNIT_ID_PARAMETER","KEYBOARD_UNIT_ID_PARAMETER","KEYBOARD_UNIT_ID_PARAMETER structure [Human Input Devices]","PKEYBOARD_UNIT_ID_PARAMETER","PKEYBOARD_UNIT_ID_PARAMETER structure pointer [Human Input Devices]","hid.keyboard_unit_id_parameter","kref_f88d7ada-5e96-4f7d-94e6-dc4196436060.xml","ntddkbd/KEYBOARD_UNIT_ID_PARAMETER","ntddkbd/PKEYBOARD_UNIT_ID_PARAMETER"]
old-location: hid\keyboard_unit_id_parameter.htm
tech.root: hid
ms.assetid: fd47b0ab-b66b-49a0-8302-2c45399d9963
ms.date: 12/05/2018
ms.keywords: '*PKEYBOARD_UNIT_ID_PARAMETER, KEYBOARD_UNIT_ID_PARAMETER, KEYBOARD_UNIT_ID_PARAMETER structure [Human Input Devices], PKEYBOARD_UNIT_ID_PARAMETER, PKEYBOARD_UNIT_ID_PARAMETER structure pointer [Human Input Devices], hid.keyboard_unit_id_parameter, kref_f88d7ada-5e96-4f7d-94e6-dc4196436060.xml, ntddkbd/KEYBOARD_UNIT_ID_PARAMETER, ntddkbd/PKEYBOARD_UNIT_ID_PARAMETER'
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
req.typenames: KEYBOARD_UNIT_ID_PARAMETER, *PKEYBOARD_UNIT_ID_PARAMETER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KEYBOARD_UNIT_ID_PARAMETER
 - ntddkbd/_KEYBOARD_UNIT_ID_PARAMETER
 - PKEYBOARD_UNIT_ID_PARAMETER
 - ntddkbd/PKEYBOARD_UNIT_ID_PARAMETER
 - KEYBOARD_UNIT_ID_PARAMETER
 - ntddkbd/KEYBOARD_UNIT_ID_PARAMETER
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
 - KEYBOARD_UNIT_ID_PARAMETER
---

# KEYBOARD_UNIT_ID_PARAMETER structure


## -description

KEYBOARD_UNIT_ID_PARAMETER specifies the unit ID that Kbdclass assigns to a keyboard.

## -struct-fields

### -field UnitId

Specifies the unit number of a keyboard device. A keyboard device name has the format \Device\KeyboardPort<i>N</i>, where the suffix <i>N </i> is the unit number of the device. For example, a device, whose name is \Device\KeyboardPort0, has a unit number of zero, and a device, whose name is \Device\KeyboardPort1, has a unit number of one.

## -remarks

Although this structure is used with IOCTL_KEYBOARD_QUERY_Xxx requests, Kbdclass does not use the <b>UnitId</b> value.

## -see-also

<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_attributes">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicators">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_indicator_translation">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="/windows/desktop/api/ntddkbd/ni-ntddkbd-ioctl_keyboard_query_typematic">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>