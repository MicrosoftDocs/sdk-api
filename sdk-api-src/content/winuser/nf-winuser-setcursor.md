---
UID: NF:winuser.SetCursor
title: SetCursor function (winuser.h)
description: Sets the cursor shape.
helpviewer_keywords: ["SetCursor","SetCursor function [Menus and Other Resources]","_win32_SetCursor","_win32_setcursor_cpp","menurc.setcursor","winui._win32_setcursor","winuser/SetCursor"]
old-location: menurc\setcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\setcursor.htm
ms.date: 12/05/2018
ms.keywords: SetCursor, SetCursor function [Menus and Other Resources], _win32_SetCursor, _win32_setcursor_cpp, menurc.setcursor, winui._win32_setcursor, winuser/SetCursor
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
 - SetCursor
 - winuser/SetCursor
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
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-RTCore-NTUser-Cursor-L1-1-0.dll
 - MinUser.dll
api_name:
 - SetCursor
---

# SetCursor function


## -description

Sets the cursor shape.

## -parameters

### -param hCursor [in, optional]

Type: <b>HCURSOR</b>

A handle to the cursor.

The cursor must have been created by either the <a href="/windows/desktop/api/winuser/nf-winuser-createcursor">CreateCursor</a> or the <a href="/windows/win32/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a> function, or loaded by either the <a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a> or the <a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a> function.

If this parameter is <b>NULL</b>, the cursor is removed from the screen.

## -returns

Type: <b>HCURSOR</b>

The return value is the handle to the previous cursor, if there was one. 

If there was no previous cursor, the return value is <b>NULL</b>.

## -remarks

The cursor is set only if the new cursor is different from the previous cursor; otherwise, the function returns immediately. 

The cursor is a shared resource. A window should set the cursor shape only when the cursor is in its client area or when the window is capturing mouse input. In systems without a mouse, the window should restore the previous cursor before the cursor leaves the client area or before it relinquishes control to another window. 

If your application must set the cursor while it is in a window, make sure the class cursor for the specified window's class is set to <b>NULL</b>. If the class cursor is not <b>NULL</b>, the system restores the class cursor each time the mouse is moved. 

The cursor is not shown on the screen if the internal cursor display count is less than zero. This occurs if the application uses the <a href="/windows/desktop/api/winuser/nf-winuser-showcursor">ShowCursor</a> function to hide the cursor more times than to show the cursor. 

#### Examples

For an example, see <a href="/windows/desktop/menurc/using-cursors">Displaying a Cursor</a>.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/menurc/cursors">Cursors</a>

<a href="/windows/desktop/menurc/using-cursors#creating-a-cursor">Creating a Cursor</a>

<a href="/windows/desktop/api/winuser/nf-winuser-createcursor">CreateCursor</a>

<a href="/windows/win32/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>

<a href="/windows/desktop/api/winuser/nf-winuser-getcursor">GetCursor</a>

<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>

<a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>

<a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>

<b>Reference</b>

<a href="/windows/desktop/api/winuser/nf-winuser-setcursorpos">SetCursorPos</a>

<a href="/windows/desktop/api/winuser/nf-winuser-showcursor">ShowCursor</a>
