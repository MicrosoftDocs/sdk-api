---
UID: NF:winuser.ClipCursor
title: ClipCursor function (winuser.h)
description: Confines the cursor to a rectangular area on the screen.
helpviewer_keywords: ["ClipCursor","ClipCursor function [Menus and Other Resources]","_win32_ClipCursor","_win32_clipcursor_cpp","menurc.clipcursor","winui._win32_clipcursor","winuser/ClipCursor"]
old-location: menurc\clipcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\clipcursor.htm
ms.date: 12/05/2018
ms.keywords: ClipCursor, ClipCursor function [Menus and Other Resources], _win32_ClipCursor, _win32_clipcursor_cpp, menurc.clipcursor, winui._win32_clipcursor, winuser/ClipCursor
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
 - ClipCursor
 - winuser/ClipCursor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-cursor-l1-1-1.dll
 - User32.dll
api_name:
 - ClipCursor
---

# ClipCursor function


## -description

Confines the cursor to a rectangular area on the screen. If a subsequent cursor position (set by the <a href="/windows/desktop/api/winuser/nf-winuser-setcursorpos">SetCursorPos</a> function or the mouse) lies outside the rectangle, the system automatically adjusts the position to keep the cursor inside the rectangular area.

## -parameters

### -param lpRect [in, optional]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to the structure that contains the screen coordinates of the upper-left and lower-right corners of the confining rectangle. If this parameter is <b>NULL</b>, the cursor is free to move anywhere on the screen.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The cursor is a shared resource. If an application confines the cursor, it must release the cursor by using <b>ClipCursor</b> before relinquishing control to another application. 

The calling process must have <b>WINSTA_WRITEATTRIBUTES</b> access to the window station. 


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-cursors">Confining a Cursor</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/cursors">Cursors</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getclipcursor">GetClipCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getcursorpos">GetCursorPos</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcursorpos">SetCursorPos</a>