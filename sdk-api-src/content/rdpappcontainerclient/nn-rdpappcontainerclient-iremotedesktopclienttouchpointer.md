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

# IRemoteDesktopClientTouchPointer interface


## -description



Provides the properties needed to control the touch pointer feature of the Remote Desktop Protocol (RDP) app container client control.



The touch pointer feature allows the Remote Desktop Protocol (RDP) app container client control to translate touch screen actions on the 
    client into equivalent mouse actions in the remote session. This feature is useful when the remote session is 
    running an operating system or application that is not optimized for touch screen. When the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> property is set, the 
    RDP app container client control will interpret certain touch gestures and translate them into mouse events in the 
    remote session. These translations make it easier for the user to simulate certain mouse actions that do not 
    readily translate to touch screen gestures, such as right-click and drag.

The following is a list of client touch-screen gestures and their corresponding remote session mouse events.
<table>
<tr>
<th>Client touch-screen gesture</th>
<th>Remote session mouse event</th>
</tr>
<tr>
<td>
Tap

</td>
<td>
Left button click

</td>
</tr>
<tr>
<td>
Drag

</td>
<td>
Cursor move

</td>
</tr>
<tr>
<td>
Press and hold with one finger, then tap with another finger to the right of the first finger

</td>
<td>
Right button click

</td>
</tr>
<tr>
<td>
Press and hold with one finger, then press and hold with another finger to the left of the first finger

</td>
<td>
Left button click and hold

</td>
</tr>
<tr>
<td>
Press and hold with one finger, then press and hold with another finger to the right of the first finger

</td>
<td>
Right button click and hold

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/EAF75483-90A4-4BB1-82A5-EFBB2219A55B">Remote Desktop ActiveX control reference</a>
 

 

