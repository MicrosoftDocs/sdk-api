---
UID: NS:winuser.tagMONITORINFOEXA
title: MONITORINFOEXA (winuser.h)
author: windows-sdk-content
description: The MONITORINFOEX structure contains information about a display monitor.The GetMonitorInfo function stores information into a MONITORINFOEX structure or a MONITORINFO structure.The MONITORINFOEX structure is a superset of the MONITORINFO structure.
old-location: gdi\monitorinfoex.htm
tech.root: gdi
ms.assetid: f296ce29-3fc8-41c9-a201-56e222aa2219
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPMONITORINFOEXA, LPMONITORINFOEX, LPMONITORINFOEX structure pointer [Windows GDI], MONITORINFOEX, MONITORINFOEX structure [Windows GDI], MONITORINFOEXA, _win32_MONITORINFOEX_str, gdi.monitorinfoex, tagMONITORINFOEXA, tagMONITORINFOEXW, winuser/LPMONITORINFOEX, winuser/MONITORINFOEX"
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

# MONITORINFOEXA structure


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

 





<a href="https://msdn.microsoft.com/025a89c2-4bbd-4c8b-8367-3735fb5b872a">GetMonitorInfo</a>



<a href="https://msdn.microsoft.com/ca8ec86f-69ba-4cf8-a867-67182a3d630d">MONITORINFO</a>



<a href="https://msdn.microsoft.com/901c8fbe-a29c-4382-80d4-5e3667a031da">Multiple Display Monitors Overview</a>



<a href="https://msdn.microsoft.com/871d0608-53a8-4b85-8c03-e7dd464015aa">Multiple Display Monitors Structures</a>
 

 

