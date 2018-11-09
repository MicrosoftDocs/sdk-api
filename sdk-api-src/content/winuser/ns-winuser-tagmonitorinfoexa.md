---
UID: NS:winuser.tagMONITORINFOEXA
title: tagMONITORINFOEXA
author: windows-sdk-content
description: The MONITORINFOEX structure contains information about a display monitor.The GetMonitorInfo function stores information into a MONITORINFOEX structure or a MONITORINFO structure.The MONITORINFOEX structure is a superset of the MONITORINFO structure.
old-location: gdi\monitorinfoex.htm
tech.root: gdi
ms.assetid: f296ce29-3fc8-41c9-a201-56e222aa2219
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPMONITORINFOEXA, LPMONITORINFOEX, LPMONITORINFOEX structure pointer [Windows GDI], MONITORINFOEX, MONITORINFOEX structure [Windows GDI], MONITORINFOEXA, _win32_MONITORINFOEX_str, gdi.monitorinfoex, tagMONITORINFOEXA, tagMONITORINFOEXW, winuser/LPMONITORINFOEX, winuser/MONITORINFOEX"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Winuser.h
api_name:
 - MONITORINFOEX
product: Windows
targetos: Windows
req.typenames: MONITORINFOEXA, *LPMONITORINFOEXA
req.redist: 
---

# tagMONITORINFOEXA structure


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

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the display monitor rectangle, expressed in virtual-screen coordinates. Note that if the monitor is not the primary display monitor, some of the rectangle's coordinates may be negative values.


#### - rcWork

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the work area rectangle of the display monitor that can be used by applications, expressed in virtual-screen coordinates. Windows uses this rectangle to maximize an application on the monitor. The rest of the area in rcMonitor contains system windows such as the task bar and side bars. Note that if the monitor is not the primary display monitor, some of the rectangle's coordinates may be negative values.


## -see-also




<a href="https://msdn.microsoft.com/025a89c2-4bbd-4c8b-8367-3735fb5b872a">GetMonitorInfo</a>



<a href="https://msdn.microsoft.com/ca8ec86f-69ba-4cf8-a867-67182a3d630d">MONITORINFO</a>



<a href="https://msdn.microsoft.com/901c8fbe-a29c-4382-80d4-5e3667a031da">Multiple Display Monitors Overview</a>



<a href="https://msdn.microsoft.com/871d0608-53a8-4b85-8c03-e7dd464015aa">Multiple Display Monitors Structures</a>
 

 

