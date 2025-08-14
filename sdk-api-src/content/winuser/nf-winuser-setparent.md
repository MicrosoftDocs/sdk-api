---
UID: NF:winuser.SetParent
title: SetParent function (winuser.h)
description: Changes the parent window of the specified child window.
helpviewer_keywords: ["SetParent","SetParent function [Windows and Messages]","_win32_SetParent","_win32_setparent_cpp","winmsg.setparent","winui._win32_setparent","winuser/SetParent"]
old-location: winmsg\setparent.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setparent.htm
ms.date: 12/05/2018
ms.keywords: SetParent, SetParent function [Windows and Messages], _win32_SetParent, _win32_setparent_cpp, winmsg.setparent, winui._win32_setparent, winuser/SetParent
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
 - SetParent
 - winuser/SetParent
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
 - SetParent
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# SetParent function


## -description

Changes the parent window of the specified child window.

## -parameters

### -param hWndChild [in]

Type: <b>HWND</b>

A handle to the child window.

### -param hWndNewParent [in, optional]

Type: <b>HWND</b>

A handle to the new parent window. If this parameter is <b>NULL</b>, the desktop window becomes the new parent window. 
					 If this parameter is <b>HWND_MESSAGE</b>, the child window becomes a <a href="/windows/desktop/winmsg/window-features">message-only window</a>.

## -returns

Type: <b>HWND</b>

If the function succeeds, the return value is a handle to the previous parent window.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application can use the <b>SetParent</b> function to set the parent window of a pop-up, overlapped, or child window.

If the window identified by the <i>hWndChild</i> parameter is visible, the system performs the appropriate redrawing and repainting. 

For compatibility reasons, <b>SetParent</b> does not modify the <b>WS_CHILD</b> or <b>WS_POPUP</b> window styles of the window whose parent is being changed. Therefore, if <i>hWndNewParent</i> is <b>NULL</b>, you should also clear the <b>WS_CHILD</b> bit and set the <b>WS_POPUP</b> style after calling <b>SetParent</b>. Conversely, if <i>hWndNewParent</i> is not <b>NULL</b> and the window was previously a child of the desktop, you should clear the <b>WS_POPUP</b> style and set the <b>WS_CHILD</b> style before calling <b>SetParent</b>. 

 When you change the parent of a window, you should synchronize the UISTATE of both windows. For more information, see <a href="/windows/desktop/menurc/wm-changeuistate">WM_CHANGEUISTATE</a> and <a href="/windows/desktop/menurc/wm-updateuistate">WM_UPDATEUISTATE</a>. 

Unexpected behavior or errors may occur if <i>hWndNewParent</i> and <i>hWndChild</i> are running in different DPI awareness modes. The table below outlines this behavior:

<table>
<tr>
<th>Operation</th>
<th>Windows 8.1</th>
<th>Windows 10 (1607 and earlier)</th>
<th>Windows 10 (1703 and later)</th>
</tr>
<tr>
<td>SetParent (In-Proc) </td>
<td>N/A </td>
<td><b>Forced reset</b> 
(of current process)</td>
<td><b>Fail</b> 
(ERROR_INVALID_STATE)</td>
</tr>
<tr>
<td>SetParent (Cross-Proc) </td>
<td><b>Forced reset</b> 
(of child window's process)</td>
<td><b>Forced reset</b> 
(of child window's process)</td>
<td><b>Forced reset</b> 
(of child window's process)</td>
</tr>
</table>
 

 For more information on DPI awareness, see <a href="/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows">the Windows High DPI documentation.</a>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getparent">GetParent</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>
