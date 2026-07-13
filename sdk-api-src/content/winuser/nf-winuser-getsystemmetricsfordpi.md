---
UID: NF:winuser.GetSystemMetricsForDpi
title: GetSystemMetricsForDpi function (winuser.h)
description: Retrieves the specified system metric or system configuration setting taking into account a provided DPI.
helpviewer_keywords: ["GetSystemMetricsForDpi","GetSystemMetricsForDpi function [High DPI]","hidpi.getsystemmetricsfordpi","winuser/GetSystemMetricsForDpi"]
old-location: hidpi\getsystemmetricsfordpi.htm
tech.root: hidpi
ms.assetid: E95BB417-81FA-4824-BE68-A1E3E003F8E0
ms.date: 12/05/2018
ms.keywords: GetSystemMetricsForDpi, GetSystemMetricsForDpi function [High DPI], hidpi.getsystemmetricsfordpi, winuser/GetSystemMetricsForDpi
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - GetSystemMetricsForDpi
 - winuser/GetSystemMetricsForDpi
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-private-l1-1-1.dll
 - ext-ms-win-rtcore-ntuser-private-l1-1-0.dll
 - ext-ms-win-ntuser-private-l1-6-3.dll
 - ext-ms-win-ntuser-private-l1-6-2.dll
 - ext-ms-win-ntuser-private-l1-6-1.dll
 - ext-ms-win-ntuser-private-l1-6-0.dll
 - ext-ms-win-ntuser-private-l1-5-0.dll
 - ext-ms-win-ntuser-private-l1-4-0.dll
 - ext-ms-win-ntuser-private-l1-3-3.dll
 - ext-ms-win-ntuser-private-l1-3-2.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetSystemMetricsForDpi
req.apiset: ext-ms-win-ntuser-private-l1-3-1 (introduced in Windows 10, version 10.0.14393)
---

# GetSystemMetricsForDpi function


## -description

Retrieves the specified system metric or system configuration setting taking into account a provided DPI.

## -parameters

### -param nIndex [in]

The system metric or configuration setting to be retrieved. See <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> for the possible values.

### -param dpi [in]

The DPI to use for scaling the metric.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function returns the same result as <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> but scales it according to an arbitrary DPI you provide if appropriate.
