---
UID: NF:winuser.GetNextWindow
title: GetNextWindow macro (winuser.h)
description: Retrieves a handle to the next or previous window in the Z-Order. The next window is below the specified window; the previous window is above.
helpviewer_keywords: ["GW_HWNDNEXT","GW_HWNDPREV","GetNextWindow","GetNextWindow function [Windows and Messages]","_win32_GetNextWindow","_win32_getnextwindow_cpp","winmsg.getnextwindow","winui._win32_getnextwindow","winuser/GetNextWindow"]
old-location: winmsg\getnextwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getnextwindow.htm
ms.date: 09/02/2025
ms.keywords: GW_HWNDNEXT, GW_HWNDPREV, GetNextWindow, GetNextWindow function [Windows and Messages], _win32_GetNextWindow, _win32_getnextwindow_cpp, winmsg.getnextwindow, winui._win32_getnextwindow, winuser/GetNextWindow
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetNextWindow
 - winuser/GetNextWindow
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
 - GetNextWindow
---

# GetNextWindow macro


## -description

Retrieves a handle to the next or previous window in the <a href="/windows/desktop/winmsg/window-features">Z-Order</a>. The next window is below the specified window; the previous window is above.

If the specified window is a topmost window, the function searches for a topmost window. If the specified window is a top-level window, the function searches for a top-level window. If the specified window is a child window, the function searches for a child window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to a window. The window handle retrieved is relative to this window, based on the value of the <i>wCmd</i> parameter.

### -param wCmd [in]

Type: <b>UINT</b>

Indicates whether the function returns a handle to the next window or the previous window. This parameter can be either of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GW_HWNDNEXT"></a><a id="gw_hwndnext"></a><dl>
<dt><b>GW_HWNDNEXT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Returns a handle to the window below the given window.

</td>
</tr>
<tr>
<td width="40%"><a id="GW_HWNDPREV"></a><a id="gw_hwndprev"></a><dl>
<dt><b>GW_HWNDPREV</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Returns a handle to the window above the given window.

</td>
</tr>
</table>

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is a window handle. If no window exists with the specified relationship to the specified window, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is implemented as a call to the <a href="/windows/desktop/api/winuser/nf-winuser-getwindow">GetWindow</a> function.


``` syntax
#define GetNextWindow(hWnd, wCmd) GetWindow(hWnd, wCmd)
```

## -syntax

```cpp
HWND GetNextWindow(
  [in] hWnd,
  [in] wCmd
);
```

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-gettopwindow">GetTopWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindow">GetWindow</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
