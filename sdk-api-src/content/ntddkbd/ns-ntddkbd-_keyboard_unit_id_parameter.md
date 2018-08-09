---
UID: NS:ntddkbd._KEYBOARD_UNIT_ID_PARAMETER
title: "_KEYBOARD_UNIT_ID_PARAMETER"
author: windows-sdk-content
description: KEYBOARD_UNIT_ID_PARAMETER specifies the unit ID that Kbdclass assigns to a keyboard.
old-location: hid\keyboard_unit_id_parameter.htm
old-project: hid
ms.assetid: fd47b0ab-b66b-49a0-8302-2c45399d9963
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PKEYBOARD_UNIT_ID_PARAMETER, KEYBOARD_UNIT_ID_PARAMETER, KEYBOARD_UNIT_ID_PARAMETER structure [Human Input Devices], PKEYBOARD_UNIT_ID_PARAMETER, PKEYBOARD_UNIT_ID_PARAMETER structure pointer [Human Input Devices], _KEYBOARD_UNIT_ID_PARAMETER, hid.keyboard_unit_id_parameter, kref_f88d7ada-5e96-4f7d-94e6-dc4196436060.xml, ntddkbd/KEYBOARD_UNIT_ID_PARAMETER, ntddkbd/PKEYBOARD_UNIT_ID_PARAMETER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: KEYBOARD_UNIT_ID_PARAMETER, *PKEYBOARD_UNIT_ID_PARAMETER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddkbd.h
api_name:
 - KEYBOARD_UNIT_ID_PARAMETER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _KEYBOARD_UNIT_ID_PARAMETER structure


## -description


KEYBOARD_UNIT_ID_PARAMETER specifies the unit ID that Kbdclass assigns to a keyboard.


## -struct-fields




### -field UnitId

Specifies the unit number of a keyboard device. A keyboard device name has the format \Device\KeyboardPort<i>N</i>, where the suffix <i>N </i>is the unit number of the device. For example, a device, whose name is \Device\KeyboardPort0, has a unit number of zero, and a device, whose name is \Device\KeyboardPort1, has a unit number of one. 


## -remarks



Although this structure is used with IOCTL_KEYBOARD_QUERY_Xxx requests, Kbdclass does not use the <b>UnitId</b> value.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541318">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541337">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541349">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541362">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>
 

 

