---
UID: NS:ntddkbd._KEYBOARD_INDICATOR_PARAMETERS
title: "_KEYBOARD_INDICATOR_PARAMETERS"
author: windows-sdk-content
description: KEYBOARD_INDICATOR_PARAMETERS specifies the state of a keyboard's indicator LEDs.
old-location: hid\keyboard_indicator_parameters.htm
tech.root: hid
ms.assetid: 68c9d24a-c1c9-4ef6-904d-6aeb68cea32a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PKEYBOARD_INDICATOR_PARAMETERS, KEYBOARD_INDICATOR_PARAMETERS, KEYBOARD_INDICATOR_PARAMETERS structure [Human Input Devices], PKEYBOARD_INDICATOR_PARAMETERS, PKEYBOARD_INDICATOR_PARAMETERS structure pointer [Human Input Devices], _KEYBOARD_INDICATOR_PARAMETERS, hid.keyboard_indicator_parameters, kref_d0dd9f49-1ccb-444f-8dd6-243f6d150ab9.xml, ntddkbd/KEYBOARD_INDICATOR_PARAMETERS, ntddkbd/PKEYBOARD_INDICATOR_PARAMETERS"
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
 - KEYBOARD_INDICATOR_PARAMETERS
product: Windows
targetos: Windows
req.typenames: KEYBOARD_INDICATOR_PARAMETERS, *PKEYBOARD_INDICATOR_PARAMETERS
req.redist: 
---

# _KEYBOARD_INDICATOR_PARAMETERS structure


## -description


KEYBOARD_INDICATOR_PARAMETERS specifies the state of a keyboard's indicator LEDs.


## -struct-fields




### -field UnitId

Specifies the unit number of a keyboard device. A keyboard device name has the format \Device\KeyboardPort<i>N</i>, where the suffix <i>N </i>is the unit number of the device. For example, a device, whose name is \Device\KeyboardPort0, has a unit number of zero, and a device, whose name is \Device\KeyboardPort1, has a unit number of one. 


### -field LedFlags

Specifies a bitwise OR of zero or more of the following LED flags: 

<table>
<tr>
<th>LED Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
KEYBOARD_CAPS_LOCK_ON

</td>
<td>
CAPS LOCK LED is on.

</td>
</tr>
<tr>
<td>
KEYBOARD_LED_INJECTED

</td>
<td>
Used by a Terminal Server. 

</td>
</tr>
<tr>
<td>
KEYBOARD_NUM_LOCK_ON

</td>
<td>
NUM LOCK LED is on.

</td>
</tr>
<tr>
<td>
KEYBOARD_SCROLL_LOCK_ON

</td>
<td>
SCROLL LOCK LED is on.

</td>
</tr>
<tr>
<td>
KEYBOARD_SHADOW

</td>
<td>
Used by a Terminal Server. 

</td>
</tr>
</table>
 


## -remarks



This structure is used with <a href="https://msdn.microsoft.com/3d70b34c-e201-40fc-99dd-cd05bdeec5f8">IOCTL_KEYBOARD_QUERY_INDICATORS</a> and <a href="https://msdn.microsoft.com/25631717-8aee-4eac-8337-46b13aa714a4">IOCTL_KEYBOARD_SET_INDICATORS</a> requests to query and set keyboard indicator LEDs.




## -see-also




<a href="https://msdn.microsoft.com/6119ca39-f740-4c8a-a7f1-eb6f30624093">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/3d70b34c-e201-40fc-99dd-cd05bdeec5f8">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/84006453-cf73-44f2-ac8b-ea03382e113d">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/0c19670b-0440-4a7a-ad87-a97d3da28e74">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/25631717-8aee-4eac-8337-46b13aa714a4">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/27c538dd-19e2-4b5a-9605-0efb0f78e008">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/fd47b0ab-b66b-49a0-8302-2c45399d9963">KEYBOARD_UNIT_ID_PARAMETER</a>
 

 

