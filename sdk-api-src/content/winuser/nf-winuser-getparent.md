---
UID: NF:winuser.GetParent
title: GetParent function (winuser.h)
description: Retrieves a handle to the specified window's parent or owner.
helpviewer_keywords: ["GetParent","GetParent function [Windows and Messages]","_win32_GetParent","_win32_getparent_cpp","winmsg.getparent","winui._win32_getparent","winuser/GetParent"]
old-location: winmsg\getparent.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getparent.htm
ms.date: 12/05/2018
ms.keywords: GetParent, GetParent function [Windows and Messages], _win32_GetParent, _win32_getparent_cpp, winmsg.getparent, winui._win32_getparent, winuser/GetParent
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
 - GetParent
 - winuser/GetParent
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
 - GetParent
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# GetParent function


## -description

Retrieves a handle to the specified window's parent or owner.

To retrieve a handle to a specified ancestor, use the <a href="/windows/desktop/api/winuser/nf-winuser-getancestor">GetAncestor</a> function.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window whose parent window handle is to be retrieved.

## -returns

Type: <b>HWND</b>

If the window is a child window, the return value is a handle to the parent window. If the window is a top-level window with the <b>WS_POPUP</b> style, the return value is a handle to the owner window. 

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

This function typically fails for one of the following reasons:


<ul>
<li>The window is a top-level window that is unowned or does not have the <b>WS_POPUP</b> style. </li>
<li>The owner window has <b>WS_POPUP</b> style.</li>
</ul>

## -remarks

To obtain a window's owner window, instead of using <b>GetParent</b>, use <a href="/windows/desktop/api/winuser/nf-winuser-getwindow">GetWindow</a> with the <b>GW_OWNER</b> flag. To obtain the parent window and not the owner, instead of using <b>GetParent</b>, use <a href="/windows/desktop/api/winuser/nf-winuser-getancestor">GetAncestor</a> with the <b>GA_PARENT</b> flag.  


#### Examples

For an example, see <a href="/windows/desktop/dlgbox/using-dialog-boxes">Initializing a Dialog Box</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getancestor">GetAncestor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindow">GetWindow</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setparent">SetParent</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>



<a href="/windows/desktop/winmsg/window-styles">Windows Styles</a>
