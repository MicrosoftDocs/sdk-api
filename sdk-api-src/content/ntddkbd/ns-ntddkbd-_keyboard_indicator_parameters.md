---
UID: NS:ntddkbd._KEYBOARD_INDICATOR_PARAMETERS
title: "_KEYBOARD_INDICATOR_PARAMETERS"
author: windows-driver-content
description: KEYBOARD_INDICATOR_PARAMETERS specifies the state of a keyboard's indicator LEDs.
old-location: hid\keyboard_indicator_parameters.htm
old-project: hid
ms.assetid: 68c9d24a-c1c9-4ef6-904d-6aeb68cea32a
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: "*PKEYBOARD_INDICATOR_PARAMETERS, KEYBOARD_INDICATOR_PARAMETERS, KEYBOARD_INDICATOR_PARAMETERS structure [Human Input Devices], PKEYBOARD_INDICATOR_PARAMETERS, PKEYBOARD_INDICATOR_PARAMETERS structure pointer [Human Input Devices], _KEYBOARD_INDICATOR_PARAMETERS, hid.keyboard_indicator_parameters, kref_d0dd9f49-1ccb-444f-8dd6-243f6d150ab9.xml, ntddkbd/KEYBOARD_INDICATOR_PARAMETERS, ntddkbd/PKEYBOARD_INDICATOR_PARAMETERS"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: KEYBOARD_INDICATOR_PARAMETERS, *PKEYBOARD_INDICATOR_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntddkbd.h
api_name:
-	KEYBOARD_INDICATOR_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

