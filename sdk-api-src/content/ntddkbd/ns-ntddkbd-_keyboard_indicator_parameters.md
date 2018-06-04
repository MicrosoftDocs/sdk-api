---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



This structure is used with <a href="https://msdn.microsoft.com/library/windows/hardware/ff541337">IOCTL_KEYBOARD_QUERY_INDICATORS</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff542067">IOCTL_KEYBOARD_SET_INDICATORS</a> requests to query and set keyboard indicator LEDs.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541318">IOCTL_KEYBOARD_QUERY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541337">IOCTL_KEYBOARD_QUERY_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541349">IOCTL_KEYBOARD_QUERY_INDICATOR_TRANSLATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541362">IOCTL_KEYBOARD_QUERY_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542067">IOCTL_KEYBOARD_SET_INDICATORS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542076">IOCTL_KEYBOARD_SET_TYPEMATIC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542352">KEYBOARD_UNIT_ID_PARAMETER</a>
 

 

