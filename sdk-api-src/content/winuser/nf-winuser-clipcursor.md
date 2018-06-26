---
UID: NF:winuser.ClipCursor
title: ClipCursor function
author: windows-sdk-content
description: Confines the cursor to a rectangular area on the screen.
old-location: menurc\clipcursor.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\clipcursor.htm
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClipCursor, ClipCursor function [Menus and Other Resources], _win32_ClipCursor, _win32_clipcursor_cpp, menurc.clipcursor, winui._win32_clipcursor, winuser/ClipCursor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ClipCursor function


## -description


Confines the cursor to a rectangular area on the screen. If a subsequent cursor position (set by the <a href="https://msdn.microsoft.com/b17cf57f-dd96-4695-a51e-ee1e1f00f85f">SetCursorPos</a> function or the mouse) lies outside the rectangle, the system automatically adjusts the position to keep the cursor inside the rectangular area. 


## -parameters




### -param lpRect [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to the structure that contains the screen coordinates of the upper-left and lower-right corners of the confining rectangle. If this parameter is <b>NULL</b>, the cursor is free to move anywhere on the screen. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The cursor is a shared resource. If an application confines the cursor, it must release the cursor by using <b>ClipCursor</b> before relinquishing control to another application. 

The calling process must have <b>WINSTA_WRITEATTRIBUTES</b> access to the window station. 


#### Examples

For an example, see <a href="using_cursors.htm">Confining a Cursor</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/f1f476b6-8306-4db5-90bf-05147af640b7">GetClipCursor</a>



<a href="https://msdn.microsoft.com/c76370d3-741a-4192-97d4-d63d2885b36b">GetCursorPos</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/b17cf57f-dd96-4695-a51e-ee1e1f00f85f">SetCursorPos</a>
 

 

