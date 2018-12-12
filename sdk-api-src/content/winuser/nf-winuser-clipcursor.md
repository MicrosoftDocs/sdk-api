---
UID: NF:winuser.ClipCursor
title: ClipCursor function
author: windows-sdk-content
description: Confines the cursor to a rectangular area on the screen.
old-location: menurc\clipcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\clipcursor.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClipCursor, ClipCursor function [Menus and Other Resources], _win32_ClipCursor, _win32_clipcursor_cpp, menurc.clipcursor, winui._win32_clipcursor, winuser/ClipCursor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
api_name:
 - ClipCursor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClipCursor function


## -description


Confines the cursor to a rectangular area on the screen. If a subsequent cursor position (set by the <a href="https://msdn.microsoft.com/en-us/library/ms648394(v=VS.85).aspx">SetCursorPos</a> function or the mouse) lies outside the rectangle, the system automatically adjusts the position to keep the cursor inside the rectangular area. 


## -parameters




### -param lpRect [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to the structure that contains the screen coordinates of the upper-left and lower-right corners of the confining rectangle. If this parameter is <b>NULL</b>, the cursor is free to move anywhere on the screen. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The cursor is a shared resource. If an application confines the cursor, it must release the cursor by using <b>ClipCursor</b> before relinquishing control to another application. 

The calling process must have <b>WINSTA_WRITEATTRIBUTES</b> access to the window station. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms648380(v=VS.85).aspx">Confining a Cursor</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646970(v=VS.85).aspx">Cursors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648387(v=VS.85).aspx">GetClipCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648390(v=VS.85).aspx">GetCursorPos</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648394(v=VS.85).aspx">SetCursorPos</a>
 

 

