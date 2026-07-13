---
UID: NS:winuser.tagMONITORINFOEXW
title: MONITORINFOEXW (winuser.h)
description: The MONITORINFOEX structure contains information about a display monitor.The GetMonitorInfo function stores information into a MONITORINFOEX structure or a MONITORINFO structure.The MONITORINFOEX structure is a superset of the MONITORINFO structure. (Unicode)
helpviewer_keywords: ["*LPMONITORINFOEXW","LPMONITORINFOEX","LPMONITORINFOEX structure pointer [Windows GDI]","MONITORINFOEX","MONITORINFOEX structure [Windows GDI]","MONITORINFOEXW","_win32_MONITORINFOEX_str","gdi.monitorinfoex","tagMONITORINFOEXA","tagMONITORINFOEXW","winuser/LPMONITORINFOEX","winuser/MONITORINFOEX"]
old-location: gdi\monitorinfoex.htm
tech.root: gdi
ms.assetid: f296ce29-3fc8-41c9-a201-56e222aa2219
ms.date: 12/05/2018
ms.keywords: '*LPMONITORINFOEXW, LPMONITORINFOEX, LPMONITORINFOEX structure pointer [Windows GDI], MONITORINFOEX, MONITORINFOEX structure [Windows GDI], MONITORINFOEXW, _win32_MONITORINFOEX_str, gdi.monitorinfoex, tagMONITORINFOEXA, tagMONITORINFOEXW, winuser/LPMONITORINFOEX, winuser/MONITORINFOEX'
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
req.typenames: MONITORINFOEXW, *LPMONITORINFOEXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMONITORINFOEXW
 - winuser/tagMONITORINFOEXW
 - LPMONITORINFOEXW
 - winuser/LPMONITORINFOEXW
 - MONITORINFOEXW
 - winuser/MONITORINFOEXW
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
 - MONITORINFOEX
---

# MONITORINFOEXW structure


## -description

The <b>MONITORINFOEX</b> structure contains information about a display monitor.

The 
        <a href="/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa">GetMonitorInfo</a> function stores information into a 
         <b>MONITORINFOEX</b>  structure or a 
        <a href="/windows/desktop/api/winuser/ns-winuser-monitorinfo">MONITORINFO</a> structure.

The 
         <b>MONITORINFOEX</b>  structure is a superset of the 
         <a href="/windows/desktop/api/winuser/ns-winuser-monitorinfo">MONITORINFO</a>  structure. The 
         <b>MONITORINFOEX</b>  structure adds a string member to contain a name for the display monitor.

## -struct-fields

### -field szDevice

A string that specifies the device name of the monitor being used.  Most applications have no use for a display monitor name, and so can save some bytes by using a <a href="/windows/desktop/api/winuser/ns-winuser-monitorinfo">MONITORINFO</a> structure.

### -field tagMONITORINFO

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa">GetMonitorInfo</a>



<a href="/windows/desktop/api/winuser/ns-winuser-monitorinfo">MONITORINFO</a>



<a href="/windows/desktop/gdi/multiple-display-monitors">Multiple Display Monitors Overview</a>



<a href="/windows/desktop/gdi/multiple-display-monitors-structures">Multiple Display Monitors Structures</a>

## -remarks

> [!NOTE]
> The winuser.h header defines MONITORINFOEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
