---
UID: NF:winuser.GetDpiForWindow
title: GetDpiForWindow function (winuser.h)
description: Returns the dots per inch (dpi) value for the specified window.
helpviewer_keywords: ["GetDpiForWindow","GetDpiForWindow function [High DPI]","hidpi.getdpiforwindow","winuser/GetDpiForWindow"]
old-location: hidpi\getdpiforwindow.htm
tech.root: hidpi
ms.assetid: E9F7BCFA-4215-44C0-95FB-57C28325720C
ms.date: 05/25/2022
ms.keywords: GetDpiForWindow, GetDpiForWindow function [High DPI], hidpi.getdpiforwindow, winuser/GetDpiForWindow
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
 - GetDpiForWindow
 - winuser/GetDpiForWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetDpiForWindow
---

## -description

Returns the dots per inch (dpi) value for the specified window.

## -parameters

### -param hwnd [in]

The window that you want to get information about.

## -returns

The DPI for the window, which depends on the [DPI_AWARENESS](/windows/win32/api/windef/ne-windef-dpi_awareness) of the window. See the **Remarks** section for more information. An invalid *hwnd* value will result in a return value of 0.

## -remarks

The following table indicates the return value of <b>GetDpiForWindow</b> based on the [DPI_AWARENESS](/windows/win32/api/windef/ne-windef-dpi_awareness) of the provided *hwnd*.

<table>
<tr>
<th>DPI_AWARENESS</th>
<th>Return value</th>
</tr>
<tr>
<td>DPI_AWARENESS_UNAWARE</td>
<td>The base value of DPI is which is set to 96 (defined as `USER_DEFAULT_SCREEN_DPI`)</td>
</tr>
<tr>
<td>DPI_AWARENESS_SYSTEM_AWARE</td>
<td>The system DPI.</td>
</tr>
<tr>
<td>DPI_AWARENESS_PER_MONITOR_AWARE</td>
<td>The DPI of the monitor where the window is located.</td>
</tr>
</table>

## Examples

See [Create a simple Direct2D application](/windows/win32/Direct2D/direct2d-quickstart).

## -see-also

* [DPI_AWARENESS](/windows/win32/api/windef/ne-windef-dpi_awareness)
* [Create a simple Direct2D application](/windows/win32/Direct2D/direct2d-quickstart)
