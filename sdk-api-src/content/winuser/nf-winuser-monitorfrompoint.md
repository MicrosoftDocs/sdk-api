---
UID: NF:winuser.MonitorFromPoint
title: MonitorFromPoint function (winuser.h)
description: The MonitorFromPoint function retrieves a handle to the display monitor that contains a specified point.
helpviewer_keywords: ["MONITOR_DEFAULTTONEAREST","MONITOR_DEFAULTTONULL","MONITOR_DEFAULTTOPRIMARY","MonitorFromPoint","MonitorFromPoint function [Windows GDI]","_win32_MonitorFromPoint","gdi.monitorfrompoint","winuser/MonitorFromPoint"]
old-location: gdi\monitorfrompoint.htm
tech.root: gdi
ms.assetid: c46281bf-7e45-4628-be92-736850225a9e
ms.date: 12/05/2018
ms.keywords: MONITOR_DEFAULTTONEAREST, MONITOR_DEFAULTTONULL, MONITOR_DEFAULTTOPRIMARY, MonitorFromPoint, MonitorFromPoint function [Windows GDI], _win32_MonitorFromPoint, gdi.monitorfrompoint, winuser/MonitorFromPoint
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
 - MonitorFromPoint
 - winuser/MonitorFromPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-sysparams-l1-1-0.dll
 - minuser.dll
api_name:
 - MonitorFromPoint
req.apiset: ext-ms-win-ntuser-sysparams-ext-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# MonitorFromPoint function


## -description

The <b>MonitorFromPoint</b> function retrieves a handle to the display monitor that contains a specified point.

## -parameters

### -param pt [in]

A <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that specifies the point of interest in virtual-screen coordinates.

### -param dwFlags [in]

Determines the function's return value if the point is not contained within any display monitor.

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
<tr>
<td width="40%"><a id="MONITOR_DEFAULTTONULL"></a><a id="monitor_defaulttonull"></a><dl>
<dt><b>MONITOR_DEFAULTTONULL</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Returns <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="MONITOR_DEFAULTTOPRIMARY"></a><a id="monitor_defaulttoprimary"></a><dl>
<dt><b>MONITOR_DEFAULTTOPRIMARY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Returns a handle to the primary display monitor.

</td>
</tr>
 
 </tr>
<tr>
<td width="40%"><a id="MONITOR_DEFAULTTONEAREST"></a><a id="monitor_defaulttonearest"></a><dl>
<dt><b>MONITOR_DEFAULTTONEAREST</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Returns a handle to the display monitor that is nearest to the point.

</td>
</tr>
</table>

## -returns

If the point is contained by a display monitor, the return value is an <b>HMONITOR</b> handle to that display monitor.

If the point is not contained by a display monitor, the return value depends on the value of <i>dwFlags</i>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-monitorfromrect">MonitorFromRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-monitorfromwindow">MonitorFromWindow</a>



<a href="/windows/desktop/gdi/multiple-display-monitors-functions">Multiple Display Monitors Functions</a>



<a href="/windows/desktop/gdi/multiple-display-monitors">Multiple Display Monitors Overview</a>
