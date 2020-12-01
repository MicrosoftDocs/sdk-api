---
UID: NS:winuser.tagMONITORINFO
title: MONITORINFO (winuser.h)
description: The MONITORINFO structure contains information about a display monitor.The GetMonitorInfo function stores information in a MONITORINFO structure or a MONITORINFOEX structure.The MONITORINFO structure is a subset of the MONITORINFOEX structure.
helpviewer_keywords: ["*LPMONITORINFO","LPMONITORINFO","LPMONITORINFO structure pointer [Windows GDI]","MONITORINFO","MONITORINFO structure [Windows GDI]","_win32_MONITORINFO_str","gdi.monitorinfo","tagMONITORINFO","winuser/LPMONITORINFO","winuser/MONITORINFO"]
old-location: gdi\monitorinfo.htm
tech.root: gdi
ms.assetid: ca8ec86f-69ba-4cf8-a867-67182a3d630d
ms.date: 12/05/2018
ms.keywords: '*LPMONITORINFO, LPMONITORINFO, LPMONITORINFO structure pointer [Windows GDI], MONITORINFO, MONITORINFO structure [Windows GDI], _win32_MONITORINFO_str, gdi.monitorinfo, tagMONITORINFO, winuser/LPMONITORINFO, winuser/MONITORINFO'
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
req.typenames: MONITORINFO, *LPMONITORINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMONITORINFO
 - winuser/tagMONITORINFO
 - LPMONITORINFO
 - winuser/LPMONITORINFO
 - MONITORINFO
 - winuser/MONITORINFO
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
 - MONITORINFO
---

# MONITORINFO structure


## -description

The <b>MONITORINFO</b> structure contains information about a display monitor.

The 
        GetMonitorInfo function stores information in a 
         <b>MONITORINFO</b>  structure or a 
        <a href="/windows/desktop/api/winuser/ns-winuser-monitorinfoexa">MONITORINFOEX</a> structure.

The 
         <b>MONITORINFO</b> structure is a subset of the 
         <a href="/windows/desktop/api/winuser/ns-winuser-monitorinfoexa">MONITORINFOEX</a>  structure. The 
         <b>MONITORINFOEX</b>  structure adds a string member to contain a name for the display monitor.

## -struct-fields

### -field cbSize

The size of the structure, in bytes.

Set this member to <code>sizeof ( MONITORINFO )</code> before calling the <a href="/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa">GetMonitorInfo</a> function. Doing so lets the function determine the type of structure you are passing to it.

### -field rcMonitor

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the display monitor rectangle, expressed in virtual-screen coordinates. Note that if the monitor is not the primary display monitor, some of the rectangle's coordinates may be negative values.

### -field rcWork

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the work area rectangle of the display monitor, expressed in virtual-screen coordinates. Note that if the monitor is not the primary display monitor, some of the rectangle's coordinates may be negative values.

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

<a href="/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa">GetMonitorInfo</a>



<a href="/windows/desktop/api/winuser/ns-winuser-monitorinfoexa">MONITORINFOEX</a>



<a href="/windows/desktop/gdi/multiple-display-monitors">Multiple Display Monitors Overview</a>



<a href="/windows/desktop/gdi/multiple-display-monitors-structures">Multiple Display Monitors Structures</a>