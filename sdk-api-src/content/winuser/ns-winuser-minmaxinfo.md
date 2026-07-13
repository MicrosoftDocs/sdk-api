---
UID: NS:winuser.tagMINMAXINFO
title: MINMAXINFO (winuser.h)
description: Contains information about a window's maximized size and position and its minimum and maximum tracking size.
helpviewer_keywords: ["*LPMINMAXINFO","*PMINMAXINFO","LPMINMAXINFO","LPMINMAXINFO structure pointer [Windows and Messages]","MINMAXINFO","MINMAXINFO structure [Windows and Messages]","PMINMAXINFO","PMINMAXINFO structure pointer [Windows and Messages]","_win32_MINMAXINFO_str","_win32_minmaxinfo_str_cpp","winmsg.minmaxinfo","winui._win32_minmaxinfo_str","winuser/LPMINMAXINFO","winuser/MINMAXINFO","winuser/PMINMAXINFO"]
old-location: winmsg\minmaxinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\minmaxinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPMINMAXINFO, *PMINMAXINFO, LPMINMAXINFO, LPMINMAXINFO structure pointer [Windows and Messages], MINMAXINFO, MINMAXINFO structure [Windows and Messages], PMINMAXINFO, PMINMAXINFO structure pointer [Windows and Messages], _win32_MINMAXINFO_str, _win32_minmaxinfo_str_cpp, winmsg.minmaxinfo, winui._win32_minmaxinfo_str, winuser/LPMINMAXINFO, winuser/MINMAXINFO, winuser/PMINMAXINFO'
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
targetos: Windows
req.typenames: MINMAXINFO, *PMINMAXINFO, *LPMINMAXINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMINMAXINFO
 - winuser/tagMINMAXINFO
 - PMINMAXINFO
 - winuser/PMINMAXINFO
 - MINMAXINFO
 - winuser/MINMAXINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MINMAXINFO
---

# MINMAXINFO structure


## -description

Contains information about a window's maximized size and position and its minimum and maximum tracking size.

## -struct-fields

### -field ptReserved

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

Reserved; do not use.

### -field ptMaxSize

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The maximized width (<b>x</b> member) and the maximized height (<b>y</b> member) of the window. For top-level windows, this value is based on the width of the primary monitor.

### -field ptMaxPosition

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The position of the left side of the maximized window (<b>x</b> member) and the position of the top of the maximized window (<b>y</b> member). For top-level windows, this value is based on the position of the primary monitor.

### -field ptMinTrackSize

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The minimum tracking width (<b>x</b> member) and the minimum tracking height (<b>y</b> member) of the window. This value can be obtained programmatically from the system metrics <b>SM_CXMINTRACK</b> and <b>SM_CYMINTRACK</b> (see the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> function).

### -field ptMaxTrackSize

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The maximum tracking width (<b>x</b> member) and the maximum tracking height (<b>y</b> member) of the window. This value is based on the size of the virtual screen and can be obtained programmatically from the system metrics <b>SM_CXMAXTRACK</b> and <b>SM_CYMAXTRACK</b> (see the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> function).

## -remarks

For systems with multiple monitors, the <b>ptMaxSize</b> and <b>ptMaxPosition</b> members describe the maximized size and position of the window on the primary monitor, even if the window ultimately maximizes onto a secondary monitor. In that case, the window manager adjusts these values to compensate for differences between the primary monitor and the monitor that displays the window. Thus, if the user leaves <b>ptMaxSize</b> untouched, a window on a monitor larger than the primary monitor maximizes to the size of the larger monitor.

## -see-also

<b>Conceptual</b>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-getminmaxinfo">WM_GETMINMAXINFO</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>