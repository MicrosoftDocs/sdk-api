---
UID: NF:winuser.MonitorFromWindow
title: MonitorFromWindow function (winuser.h)
description: The MonitorFromWindow function retrieves a handle to the display monitor that has the largest area of intersection with the bounding rectangle of a specified window.
helpviewer_keywords: ["MONITOR_DEFAULTTONEAREST","MONITOR_DEFAULTTONULL","MONITOR_DEFAULTTOPRIMARY","MonitorFromWindow","MonitorFromWindow function [Windows GDI]","_win32_MonitorFromWindow","gdi.monitorfromwindow","winuser/MonitorFromWindow"]
old-location: gdi\monitorfromwindow.htm
tech.root: gdi
ms.assetid: fe6505c9-b481-4fec-ae9d-995943234a3a
ms.date: 12/05/2018
ms.keywords: MONITOR_DEFAULTTONEAREST, MONITOR_DEFAULTTONULL, MONITOR_DEFAULTTOPRIMARY, MonitorFromWindow, MonitorFromWindow function [Windows GDI], _win32_MonitorFromWindow, gdi.monitorfromwindow, winuser/MonitorFromWindow
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MonitorFromWindow
 - winuser/MonitorFromWindow
dev_langs:
 - c++
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
req.apiset: ext-ms-win-ntuser-sysparams-ext-l1-1-1 (introduced in Windows 10, version 10.0.14393)
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

<a href="/windows/desktop/api/winuser/nf-winuser-monitorfrompoint">MonitorFromPoint</a>



<a href="/windows/desktop/api/winuser/nf-winuser-monitorfromrect">MonitorFromRect</a>



<a href="/windows/desktop/gdi/multiple-display-monitors-functions">Multiple Display Monitors Functions</a>



<a href="/windows/desktop/gdi/multiple-display-monitors">Multiple Display Monitors Overview</a>
