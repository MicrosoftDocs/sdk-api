---
UID: NF:winuser.GetCursorPos
title: GetCursorPos function (winuser.h)
description: Retrieves the position of the mouse cursor, in screen coordinates.helpviewer_keywords: ["GetCursorPos","GetCursorPos function [Menus and Other Resources]","_win32_GetCursorPos","_win32_getcursorpos_cpp","menurc.getcursorpos","winui._win32_getcursorpos","winuser/GetCursorPos"]
old-location: menurc\getcursorpos.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getcursorpos.htm
ms.date: 12/05/2018
ms.keywords: GetCursorPos, GetCursorPos function [Menus and Other Resources], _win32_GetCursorPos, _win32_getcursorpos_cpp, menurc.getcursorpos, winui._win32_getcursorpos, winuser/GetCursorPos
f1_keywords:
- winuser/GetCursorPos
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCursorPos function


## -description


Retrieves the position of the mouse cursor, in screen coordinates.


## -parameters




### -param lpPoint [out]

Type: <b>LPPOINT</b>

A pointer to a <a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure that receives the screen coordinates of the cursor.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful or zero otherwise. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The cursor position is always specified in screen coordinates and is not affected by the mapping mode of the window that contains the cursor.

The calling process must have <b>WINSTA_READATTRIBUTES</b> access to the window station.

The input desktop must be the current desktop when you call <b>GetCursorPos</b>. Call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-openinputdesktop">OpenInputDesktop</a> to determine whether the current desktop is the input desktop. If it is not, call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddesktop">SetThreadDesktop</a> with the <b>HDESK</b> returned by <b>OpenInputDesktop</b> to switch to that desktop.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/menurc/using-cursors">Using the Keyboard to Move the Cursor</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-clipcursor">ClipCursor</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/cursors">Cursors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getcursorinfo">GetCursorInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getmessagepos">GetMessagePos</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setcursorpos">SetCursorPos</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-showcursor">ShowCursor</a>
 

 

