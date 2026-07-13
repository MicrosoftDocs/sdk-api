---
UID: NF:winuser.GetMonitorInfoA
title: GetMonitorInfoA function (winuser.h)
description: The GetMonitorInfo function retrieves information about a display monitor. (ANSI)
helpviewer_keywords: ["GetMonitorInfoA", "winuser/GetMonitorInfoA"]
old-location: gdi\getmonitorinfo.htm
tech.root: gdi
ms.assetid: 025a89c2-4bbd-4c8b-8367-3735fb5b872a
ms.date: 12/05/2018
ms.keywords: GetMonitorInfo, GetMonitorInfo function [Windows GDI], GetMonitorInfoA, GetMonitorInfoW, _win32_GetMonitorInfo, gdi.getmonitorinfo, winuser/GetMonitorInfo, winuser/GetMonitorInfoA, winuser/GetMonitorInfoW
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetMonitorInfoA
 - winuser/GetMonitorInfoA
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
 - api-ms-win-ntuser-sysparams-l1-1-0.dll
 - Ext-MS-Win-NTUser-SysParams-Ext-L1-1-0.dll
api_name:
 - GetMonitorInfo
 - GetMonitorInfoA
 - GetMonitorInfoW
req.apiset: ext-ms-win-ntuser-sysparams-ext-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# GetMonitorInfoA function


## -description

The <b>GetMonitorInfo</b> function retrieves information about a display monitor.

## -parameters

### -param hMonitor [in]

A handle to the display monitor of interest.

### -param lpmi [out]

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-monitorinfo">MONITORINFO</a> or <a href="/windows/desktop/api/winuser/ns-winuser-monitorinfoexa">MONITORINFOEX</a> structure that receives information about the specified display monitor.

You must set the <b>cbSize</b> member of the structure to sizeof(MONITORINFO) or sizeof(MONITORINFOEX) before calling the <b>GetMonitorInfo</b> function. Doing so lets the function determine the type of structure you are passing to it.

The <a href="/windows/desktop/api/winuser/ns-winuser-monitorinfoexa">MONITORINFOEX</a> structure is a superset of the <a href="/windows/desktop/api/winuser/ns-winuser-monitorinfo">MONITORINFO</a> structure. It has one additional member: a string that contains a name for the display monitor. Most applications have no use for a display monitor name, and so can save some bytes by using a <b>MONITORINFO</b> structure.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/api/winuser/ns-winuser-monitorinfo">MONITORINFO</a>



<a href="/windows/desktop/api/winuser/ns-winuser-monitorinfoexa">MONITORINFOEX</a>



<a href="/windows/desktop/gdi/multiple-display-monitors-functions">Multiple Display Monitors Functions</a>



<a href="/windows/desktop/gdi/multiple-display-monitors">Multiple Display Monitors Overview</a>

## -remarks

> [!NOTE]
> The winuser.h header defines GetMonitorInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
