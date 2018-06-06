---
UID: NF:winuser.GetMonitorInfoA
title: GetMonitorInfoA function
author: windows-sdk-content
description: The GetMonitorInfo function retrieves information about a display monitor.
old-location: gdi\getmonitorinfo.htm
old-project: gdi
ms.assetid: 025a89c2-4bbd-4c8b-8367-3735fb5b872a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetMonitorInfo, GetMonitorInfo function [Windows GDI], GetMonitorInfoA, GetMonitorInfoW, _win32_GetMonitorInfo, gdi.getmonitorinfo, winuser/GetMonitorInfo, winuser/GetMonitorInfoA, winuser/GetMonitorInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetMonitorInfoW (Unicode) and GetMonitorInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-RTCore-NTUser-sysparams-l1-1-0.dll
 - minuser.dll
 - api-ms-win-ntuser-sysparams-l1-1-0.dll
 - Ext-MS-Win-NTUser-SysParams-Ext-L1-1-0.dll
api_name:
 - GetMonitorInfo
 - GetMonitorInfoA
 - GetMonitorInfoW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetMonitorInfoA function


## -description


The <b>GetMonitorInfo</b> function retrieves information about a display monitor.


## -parameters




### -param hMonitor [in]

A handle to the display monitor of interest.


### -param lpmi [out]

A pointer to a <a href="https://msdn.microsoft.com/ca8ec86f-69ba-4cf8-a867-67182a3d630d">MONITORINFO</a> or <a href="https://msdn.microsoft.com/f296ce29-3fc8-41c9-a201-56e222aa2219">MONITORINFOEX</a> structure that receives information about the specified display monitor.

You must set the <b>cbSize</b> member of the structure to sizeof(MONITORINFO) or sizeof(MONITORINFOEX) before calling the <b>GetMonitorInfo</b> function. Doing so lets the function determine the type of structure you are passing to it.

The <a href="https://msdn.microsoft.com/f296ce29-3fc8-41c9-a201-56e222aa2219">MONITORINFOEX</a> structure is a superset of the <a href="https://msdn.microsoft.com/ca8ec86f-69ba-4cf8-a867-67182a3d630d">MONITORINFO</a> structure. It has one additional member: a string that contains a name for the display monitor. Most applications have no use for a display monitor name, and so can save some bytes by using a <b>MONITORINFO</b> structure.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/ca8ec86f-69ba-4cf8-a867-67182a3d630d">MONITORINFO</a>



<a href="https://msdn.microsoft.com/f296ce29-3fc8-41c9-a201-56e222aa2219">MONITORINFOEX</a>



<a href="https://msdn.microsoft.com/a64b256c-e7a1-4ee2-a346-4b7abcab9e90">Multiple Display Monitors Functions</a>



<a href="https://msdn.microsoft.com/901c8fbe-a29c-4382-80d4-5e3667a031da">Multiple Display Monitors Overview</a>
 

 

