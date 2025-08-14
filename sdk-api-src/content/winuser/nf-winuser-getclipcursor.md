---
UID: NF:winuser.GetClipCursor
title: GetClipCursor function (winuser.h)
description: Retrieves the screen coordinates of the rectangular area to which the cursor is confined.
helpviewer_keywords: ["GetClipCursor","GetClipCursor function [Menus and Other Resources]","_win32_GetClipCursor","_win32_getclipcursor_cpp","menurc.getclipcursor","winui._win32_getclipcursor","winuser/GetClipCursor"]
old-location: menurc\getclipcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getclipcursor.htm
ms.date: 12/05/2018
ms.keywords: GetClipCursor, GetClipCursor function [Menus and Other Resources], _win32_GetClipCursor, _win32_getclipcursor_cpp, menurc.getclipcursor, winui._win32_getclipcursor, winuser/GetClipCursor
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
 - GetClipCursor
 - winuser/GetClipCursor
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
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-RTCore-NTUser-Cursor-L1-1-0.dll
 - MinUser.dll
api_name:
 - GetClipCursor
---

# GetClipCursor function


## -description

Retrieves the screen coordinates of the rectangular area to which the cursor is confined.

## -parameters

### -param lpRect [out]

Type: <b>LPRECT</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the screen coordinates of the confining rectangle. The structure receives the dimensions of the screen if the cursor is not confined to a rectangle.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The cursor is a shared resource. If an application confines the cursor with the <a href="/windows/desktop/api/winuser/nf-winuser-clipcursor">ClipCursor</a> function, it must later release the cursor by using <b>ClipCursor</b> before relinquishing control to another application. 

The calling process must have <b>WINSTA_READATTRIBUTES</b> access to the window station. 


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-cursors">Confining a Cursor</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-clipcursor">ClipCursor</a>



<b>Conceptual</b>



<a href="/windows/desktop/menurc/cursors">Cursors</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getcursorpos">GetCursorPos</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>