---
UID: NF:winuser.GetWindow
title: GetWindow function (winuser.h)
description: Retrieves a handle to a window that has the specified relationship (Z-Order or owner) to the specified window.
helpviewer_keywords: ["GW_CHILD","GW_ENABLEDPOPUP","GW_HWNDFIRST","GW_HWNDLAST","GW_HWNDNEXT","GW_HWNDPREV","GW_OWNER","GetWindow","GetWindow function [Windows and Messages]","_win32_GetWindow","_win32_getwindow_cpp","winmsg.getwindow","winui._win32_getwindow","winuser/GetWindow"]
old-location: winmsg\getwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindow.htm
ms.date: 12/05/2018
ms.keywords: GW_CHILD, GW_ENABLEDPOPUP, GW_HWNDFIRST, GW_HWNDLAST, GW_HWNDNEXT, GW_HWNDPREV, GW_OWNER, GetWindow, GetWindow function [Windows and Messages], _win32_GetWindow, _win32_getwindow_cpp, winmsg.getwindow, winui._win32_getwindow, winuser/GetWindow
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
 - GetWindow
 - winuser/GetWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# GetWindow function


## -description

Retrieves a handle to a window that has the specified relationship (<a href="/windows/desktop/winmsg/window-features">Z-Order</a> or owner) to the specified window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to a window. The window handle retrieved is relative to this window, based on the value of the <i>uCmd</i> parameter.

### -param uCmd [in]

Type: <b>UINT</b>

The relationship between the specified window and the window whose handle is to be retrieved. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GW_CHILD"></a><a id="gw_child"></a><dl>
<dt><b>GW_CHILD</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The retrieved handle identifies the child window at the top of the Z order, if the specified window is a parent window; otherwise, the retrieved handle is <b>NULL</b>. The function examines only child windows of the specified window. It does not examine descendant windows.

</td>
</tr>
<tr>
<td width="40%"><a id="GW_ENABLEDPOPUP"></a><a id="gw_enabledpopup"></a><dl>
<dt><b>GW_ENABLEDPOPUP</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The retrieved handle identifies the enabled popup window owned by the specified window (the search uses the first such window found using <b>GW_HWNDNEXT</b>); otherwise, if there are no enabled popup windows, the retrieved handle is that of the specified window. 

</td>
</tr>
<tr>
<td width="40%"><a id="GW_HWNDFIRST"></a><a id="gw_hwndfirst"></a><dl>
<dt><b>GW_HWNDFIRST</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The retrieved handle identifies the window of the same type that is highest in the Z order.

If the specified window is a topmost window, the handle identifies a topmost window. If the specified window is a top-level window, the handle identifies a top-level window. If the specified window is a child window, the handle identifies a sibling window.

</td>
</tr>
<tr>
<td width="40%"><a id="GW_HWNDLAST"></a><a id="gw_hwndlast"></a><dl>
<dt><b>GW_HWNDLAST</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The retrieved handle identifies the window of the same type that is lowest in the Z order.

If the specified window is a topmost window, the handle identifies a topmost window. If the specified window is a top-level window, the handle identifies a top-level window. If the specified window is a child window, the handle identifies a sibling window.

</td>
</tr>
<tr>
<td width="40%"><a id="GW_HWNDNEXT"></a><a id="gw_hwndnext"></a><dl>
<dt><b>GW_HWNDNEXT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The retrieved handle identifies the window below the specified window in the Z order.

If the specified window is a topmost window, the handle identifies a topmost window. If the specified window is a top-level window, the handle identifies a top-level window. If the specified window is a child window, the handle identifies a sibling window.

</td>
</tr>
<tr>
<td width="40%"><a id="GW_HWNDPREV"></a><a id="gw_hwndprev"></a><dl>
<dt><b>GW_HWNDPREV</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The retrieved handle identifies the window above the specified window in the Z order.

If the specified window is a topmost window, the handle identifies a topmost window. If the specified window is a top-level window, the handle identifies a top-level window. If the specified window is a child window, the handle identifies a sibling window.

</td>
</tr>
<tr>
<td width="40%"><a id="GW_OWNER"></a><a id="gw_owner"></a><dl>
<dt><b>GW_OWNER</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The retrieved handle identifies the specified window's owner window, if any. For more information, see <a href="/windows/desktop/winmsg/window-features">Owned Windows</a>. 

</td>
</tr>
</table>

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is a window handle. If no window exists with the specified relationship to the specified window, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <a href="/windows/desktop/api/winuser/nf-winuser-enumchildwindows">EnumChildWindows</a> function is more reliable than calling <b>GetWindow</b> in a loop. An application that calls <b>GetWindow</b> to perform this task risks being caught in an infinite loop or referencing a handle to a window that has been destroyed.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-enumchildwindows">EnumChildWindows</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
