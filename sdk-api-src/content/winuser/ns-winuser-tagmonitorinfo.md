---
UID: NS:winuser.tagMONITORINFO
title: tagMONITORINFO
author: windows-sdk-content
description: The MONITORINFO structure contains information about a display monitor.The GetMonitorInfo function stores information in a MONITORINFO structure or a MONITORINFOEX structure.The MONITORINFO structure is a subset of the MONITORINFOEX structure.
old-location: gdi\monitorinfo.htm
tech.root: gdi
ms.assetid: ca8ec86f-69ba-4cf8-a867-67182a3d630d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPMONITORINFO, LPMONITORINFO, LPMONITORINFO structure pointer [Windows GDI], MONITORINFO, MONITORINFO structure [Windows GDI], _win32_MONITORINFO_str, gdi.monitorinfo, tagMONITORINFO, winuser/LPMONITORINFO, winuser/MONITORINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MONITORINFO
product: Windows
targetos: Windows
req.typenames: MONITORINFO, *LPMONITORINFO
req.redist: 
---

# tagMONITORINFO structure


## -description



The <b>MONITORINFO</b> structure contains information about a display monitor.

The 
        GetMonitorInfo function stores information in a 
         <b>MONITORINFO</b>  structure or a 
        <a href="https://msdn.microsoft.com/f296ce29-3fc8-41c9-a201-56e222aa2219">MONITORINFOEX</a> structure.

The 
         <b>MONITORINFO</b> structure is a subset of the 
         <a href="https://msdn.microsoft.com/f296ce29-3fc8-41c9-a201-56e222aa2219">MONITORINFOEX</a>  structure. The 
         <b>MONITORINFOEX</b>  structure adds a string member to contain a name for the display monitor.




## -struct-fields




### -field cbSize

The size of the structure, in bytes.

Set this member to <code>sizeof ( MONITORINFO )</code> before calling the <a href="https://msdn.microsoft.com/025a89c2-4bbd-4c8b-8367-3735fb5b872a">GetMonitorInfo</a> function. Doing so lets the function determine the type of structure you are passing to it.


### -field rcMonitor

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the display monitor rectangle, expressed in virtual-screen coordinates. Note that if the monitor is not the primary display monitor, some of the rectangle's coordinates may be negative values.


### -field rcWork

A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the work area rectangle of the display monitor, expressed in virtual-screen coordinates. Note that if the monitor is not the primary display monitor, some of the rectangle's coordinates may be negative values.


### -field dwFlags

A set of flags that represent attributes of the display monitor.

The following flag is defined.

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
 


## -see-also




<a href="https://msdn.microsoft.com/025a89c2-4bbd-4c8b-8367-3735fb5b872a">GetMonitorInfo</a>



<a href="https://msdn.microsoft.com/f296ce29-3fc8-41c9-a201-56e222aa2219">MONITORINFOEX</a>



<a href="https://msdn.microsoft.com/901c8fbe-a29c-4382-80d4-5e3667a031da">Multiple Display Monitors Overview</a>



<a href="https://msdn.microsoft.com/871d0608-53a8-4b85-8c03-e7dd464015aa">Multiple Display Monitors Structures</a>
 

 

