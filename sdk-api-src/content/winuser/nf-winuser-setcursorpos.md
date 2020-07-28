---
UID: NF:winuser.SetCursorPos
title: SetCursorPos function (winuser.h)
description: Moves the cursor to the specified screen coordinates.
helpviewer_keywords: ["SetCursorPos","SetCursorPos function [Menus and Other Resources]","_win32_SetCursorPos","_win32_setcursorpos_cpp","menurc.setcursorpos","winui._win32_setcursorpos","winuser/SetCursorPos"]
old-location: menurc\setcursorpos.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\setcursorpos.htm
ms.date: 12/05/2018
ms.keywords: SetCursorPos, SetCursorPos function [Menus and Other Resources], _win32_SetCursorPos, _win32_setcursorpos_cpp, menurc.setcursorpos, winui._win32_setcursorpos, winuser/SetCursorPos
f1_keywords:
- winuser/SetCursorPos
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
- SetCursorPos
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetCursorPos function


## -description


Moves the cursor to the specified screen coordinates. If the new coordinates are not within the screen rectangle set by the most recent <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-clipcursor">ClipCursor</a> function call, the system automatically adjusts the coordinates so that the cursor stays within the rectangle. 


## -parameters




### -param X [in]

Type: <b>int</b>

The new x-coordinate of the cursor, in screen coordinates. 


### -param Y [in]

Type: <b>int</b>

The new y-coordinate of the cursor, in screen coordinates. 


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful or zero otherwise. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The cursor is a shared resource. A window should move the cursor only when the cursor is in the window's client area.

The calling process must have <b>WINSTA_WRITEATTRIBUTES</b> access to the window station.

The input desktop must be the current desktop when you call <b>SetCursorPos</b>. Call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-openinputdesktop">OpenInputDesktop</a> to determine whether the current desktop is the input desktop. If it is not, call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddesktop">SetThreadDesktop</a> with the <b>HDESK</b> returned by <b>OpenInputDesktop</b> to switch to that desktop.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/menurc/using-cursors">Using the Keyboard to Move the Cursor</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-clipcursor">ClipCursor</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/cursors">Cursors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getcursorpos">GetCursorPos</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setcaretpos">SetCaretPos</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-showcursor">ShowCursor</a>
 

 

