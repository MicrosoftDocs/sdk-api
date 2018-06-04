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

# tagMONITORINFOEXW structure


## -description



The <b>MONITORINFOEX</b> structure contains information about a display monitor.

The 
        <a href="https://msdn.microsoft.com/025a89c2-4bbd-4c8b-8367-3735fb5b872a">GetMonitorInfo</a> function stores information into a 
         <b>MONITORINFOEX</b>  structure or a 
        <a href="https://msdn.microsoft.com/ca8ec86f-69ba-4cf8-a867-67182a3d630d">MONITORINFO</a> structure.

The 
         <b>MONITORINFOEX</b>  structure is a superset of the 
         <a href="https://msdn.microsoft.com/ca8ec86f-69ba-4cf8-a867-67182a3d630d">MONITORINFO</a>  structure. The 
         <b>MONITORINFOEX</b>  structure adds a string member to contain a name for the display monitor.




## -struct-fields




### -field szDevice

A string that specifies the device name of the monitor being used.  Most applications have no use for a display monitor name, and so can save some bytes by using a <a href="https://msdn.microsoft.com/ca8ec86f-69ba-4cf8-a867-67182a3d630d">MONITORINFO</a> structure.


### -field tagMONITORINFO

 




#### - cbSize

The size, in bytes, of the structure.

Set this member to <code>sizeof(MONITORINFOEX)</code> before calling the <a href="https://msdn.microsoft.com/025a89c2-4bbd-4c8b-8367-3735fb5b872a">GetMonitorInfo</a> function. Doing so lets the function determine the type of structure you are passing to it.


#### - dwFlags

The attributes of the display monitor.

This member can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>MONITORINFOF_PRIMARY</td>
<td>This is the primary display monitor.</td>
</tr>
</table>
 


#### - rcMonitor

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the display monitor rectangle, expressed in virtual-screen coordinates. Note that if the monitor is not the primary display monitor, some of the rectangle's coordinates may be negative values.


#### - rcWork

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the work area rectangle of the display monitor that can be used by applications, expressed in virtual-screen coordinates. Windows uses this rectangle to maximize an application on the monitor. The rest of the area in rcMonitor contains system windows such as the task bar and side bars. Note that if the monitor is not the primary display monitor, some of the rectangle's coordinates may be negative values.


## -see-also




<a href="https://msdn.microsoft.com/025a89c2-4bbd-4c8b-8367-3735fb5b872a">GetMonitorInfo</a>



<a href="https://msdn.microsoft.com/ca8ec86f-69ba-4cf8-a867-67182a3d630d">MONITORINFO</a>



<a href="https://msdn.microsoft.com/901c8fbe-a29c-4382-80d4-5e3667a031da">Multiple Display Monitors Overview</a>



<a href="https://msdn.microsoft.com/871d0608-53a8-4b85-8c03-e7dd464015aa">Multiple Display Monitors Structures</a>
 

 

