---
UID: NF:winuser.GetCursorPos
title: GetCursorPos function (winuser.h)
description: Retrieves the position of the mouse cursor, in screen coordinates.
helpviewer_keywords: ["GetCursorPos","GetCursorPos function [Menus and Other Resources]","_win32_GetCursorPos","_win32_getcursorpos_cpp","menurc.getcursorpos","winui._win32_getcursorpos","winuser/GetCursorPos"]
old-location: menurc\getcursorpos.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getcursorpos.htm
ms.date: 12/05/2018
ms.keywords: GetCursorPos, GetCursorPos function [Menus and Other Resources], _win32_GetCursorPos, _win32_getcursorpos_cpp, menurc.getcursorpos, winui._win32_getcursorpos, winuser/GetCursorPos
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
 - GetCursorPos
 - winuser/GetCursorPos
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-l1-1-0.dll
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetCursorPos
req.apiset: ext-ms-win-ntuser-window-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# GetCursorPos function


## -description

Retrieves the position of the mouse cursor, in screen coordinates.

## -parameters

### -param lpPoint [out]

Type: <b>LPPOINT</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that receives the screen coordinates of the cursor.

## -returns

Type: <b>BOOL</b>

Returns nonzero if successful or zero otherwise. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The cursor position is always specified in screen coordinates and is not affected by the mapping mode of the window that contains the cursor.

The calling process must have <b>WINSTA_READATTRIBUTES</b> access to the window station.

The input desktop must be the current desktop when you call <b>GetCursorPos</b>. Call <a href="/windows/desktop/api/winuser/nf-winuser-openinputdesktop">OpenInputDesktop</a> to determine whether the current desktop is the input desktop. If it is not, call <a href="/windows/desktop/api/winuser/nf-winuser-setthreaddesktop">SetThreadDesktop</a> with the <b>HDESK</b> returned by <b>OpenInputDesktop</b> to switch to that desktop.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-cursors">Using the Keyboard to Move the Cursor</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-clipcursor">ClipCursor</a>



<b>Conceptual</b>



<a href="/windows/desktop/menurc/cursors">Cursors</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getcursorinfo">GetCursorInfo</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessagepos">GetMessagePos</a>



<b>Other Resources</b>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setcursorpos">SetCursorPos</a>



<a href="/windows/desktop/api/winuser/nf-winuser-showcursor">ShowCursor</a>
