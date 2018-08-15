---
UID: NS:ntddkbd._KEYBOARD_TYPEMATIC_PARAMETERS
title: "_KEYBOARD_TYPEMATIC_PARAMETERS"
author: windows-sdk-content
description: KEYBOARD_TYPEMATIC_PARAMETERS specifies a keyboard's typematic settings.
old-location: hid\keyboard_typematic_parameters.htm
old-project: hid
ms.assetid: 4bbf1699-1ba9-4569-97ac-156a91405586
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PKEYBOARD_TYPEMATIC_PARAMETERS, KEYBOARD_TYPEMATIC_PARAMETERS, KEYBOARD_TYPEMATIC_PARAMETERS structure [Human Input Devices], PKEYBOARD_TYPEMATIC_PARAMETERS, PKEYBOARD_TYPEMATIC_PARAMETERS structure pointer [Human Input Devices], _KEYBOARD_TYPEMATIC_PARAMETERS, hid.keyboard_typematic_parameters, kref_1ef2a956-3ef3-40fc-be6e-4ce8c97f2e52.xml, ntddkbd/KEYBOARD_TYPEMATIC_PARAMETERS, ntddkbd/PKEYBOARD_TYPEMATIC_PARAMETERS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntddkbd.h
req.include-header: Ntddkbd.h
req.redist: 
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
req.typenames: KEYBOARD_TYPEMATIC_PARAMETERS, *PKEYBOARD_TYPEMATIC_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddkbd.h
api_name:
 - KEYBOARD_TYPEMATIC_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _KEYBOARD_TYPEMATIC_PARAMETERS structure


## -description


KEYBOARD_TYPEMATIC_PARAMETERS specifies a keyboard's typematic settings.


## -struct-fields




### -field UnitId

Specifies the unit number of a keyboard device. A keyboard device name has the format \Device\KeyboardPort<i>N</i>, where the suffix <i>N </i>is the unit number of the device. For example, a device, whose name is \Device\KeyboardPort0, has a unit number of zero, and a device, whose name is \Device\KeyboardPort1, has a unit number of one. 


### -field Rate

Specifies the rate at which character output from a keyboard repeats, in characters per second, after a key is pressed and continuously held down. The minimum possible value is KEYBOARD_TYPEMATIC_RATE_MINIMUM and the maximum possible value is KEYBOARD_TYPEMATIC_RATE_MAXIMUM. The default value is KEYBOARD_TYPEMATIC_RATE_DEFAULT.


### -field Delay

Specifies the amount of time that must elapse, in milliseconds, after a key is pressed and continuously held down, before the character output from a keyboard begins to repeat. The minimum possible delay is KEYBOARD_TYPEMATIC_DELAY_MINIMUM and the maximum possible delay is KEYBOARD_TYPEMATIC_DELAY_MAXIMUM. The default value is KEYBOARD_TYPEMATIC_DELAY_DEFAULT.


## -remarks



This structure is used with <a href="https://msdn.microsoft.com/0c19670b-0440-4a7a-ad87-a97d3da28e74">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a> and <a href="https://msdn.microsoft.com/27c538dd-19e2-4b5a-9605-0efb0f78e008">IOCTL_KEYBOARD_SET_TYPEMATIC</a> requests to query and set a keyboard's typematic settings. 




## -see-also




<a href="https://msdn.microsoft.com/6119ca39-f740-4c8a-a7f1-eb6f30624093">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/3d70b34c-e201-40fc-99dd-cd05bdeec5f8">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/84006453-cf73-44f2-ac8b-ea03382e113d">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/0c19670b-0440-4a7a-ad87-a97d3da28e74">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/25631717-8aee-4eac-8337-46b13aa714a4">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/27c538dd-19e2-4b5a-9605-0efb0f78e008">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/fd47b0ab-b66b-49a0-8302-2c45399d9963">KEYBOARD_UNIT_ID_PARAMETER</a>
 

 

