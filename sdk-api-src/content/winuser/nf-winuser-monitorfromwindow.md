---
UID: NF:winuser.MonitorFromWindow
title: MonitorFromWindow function
author: windows-sdk-content
description: The MonitorFromWindow function retrieves a handle to the display monitor that has the largest area of intersection with the bounding rectangle of a specified window.
old-location: gdi\monitorfromwindow.htm
tech.root: gdi
ms.assetid: fe6505c9-b481-4fec-ae9d-995943234a3a
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: MONITOR_DEFAULTTONEAREST, MONITOR_DEFAULTTONULL, MONITOR_DEFAULTTOPRIMARY, MonitorFromWindow, MonitorFromWindow function [Windows GDI], _win32_MonitorFromWindow, gdi.monitorfromwindow, winuser/MonitorFromWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-RTCore-NTUser-sysparams-l1-1-0.dll
 - minuser.dll
api_name:
 - MonitorFromWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MonitorFromWindow function


## -description


The <b>MonitorFromWindow</b> function retrieves a handle to the display monitor that has the largest area of intersection with the bounding rectangle of a specified window.


## -parameters




### -param hwnd [in]

A handle to the window of interest.


### -param dwFlags [in]

Determines the function's return value if the window does not intersect any display monitor.

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MONITOR_DEFAULTTONEAREST"></a><a id="monitor_defaulttonearest"></a><dl>
<dt><b>MONITOR_DEFAULTTONEAREST</b></dt>
</dl>
</td>
<td width="60%">
Returns a handle to the display monitor that is nearest to the window.

</td>
</tr>
<tr>
<td width="40%"><a id="MONITOR_DEFAULTTONULL"></a><a id="monitor_defaulttonull"></a><dl>
<dt><b>MONITOR_DEFAULTTONULL</b></dt>
</dl>
</td>
<td width="60%">
Returns <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MONITOR_DEFAULTTOPRIMARY"></a><a id="monitor_defaulttoprimary"></a><dl>
<dt><b>MONITOR_DEFAULTTOPRIMARY</b></dt>
</dl>
</td>
<td width="60%">
Returns a handle to the primary display monitor.

</td>
</tr>
</table>
 


## -returns



If the window intersects one or more display monitor rectangles, the return value is an <b>HMONITOR</b> handle to the display monitor that has the largest area of intersection with the window.

If the window does not intersect a display monitor, the return value depends on the value of <i>dwFlags</i>.




## -remarks



If the window is currently minimized, <b>MonitorFromWindow</b> uses the rectangle of the window before it was minimized.




## -see-also




<a href="https://msdn.microsoft.com/c46281bf-7e45-4628-be92-736850225a9e">MonitorFromPoint</a>



<a href="https://msdn.microsoft.com/81c3fffb-bbc9-4adb-bb6b-edd59f7a77b4">MonitorFromRect</a>



<a href="https://msdn.microsoft.com/a64b256c-e7a1-4ee2-a346-4b7abcab9e90">Multiple Display Monitors Functions</a>



<a href="https://msdn.microsoft.com/901c8fbe-a29c-4382-80d4-5e3667a031da">Multiple Display Monitors Overview</a>
 

 

