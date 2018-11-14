---
UID: NF:winuser.SetCursorPos
title: SetCursorPos function
author: windows-sdk-content
description: Moves the cursor to the specified screen coordinates.
old-location: menurc\setcursorpos.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\setcursorpos.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SetCursorPos, SetCursorPos function [Menus and Other Resources], _win32_SetCursorPos, _win32_setcursorpos_cpp, menurc.setcursorpos, winui._win32_setcursorpos, winuser/SetCursorPos
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetCursorPos
: 
---

# SetCursorPos function


## -description


Moves the cursor to the specified screen coordinates. If the new coordinates are not within the screen rectangle set by the most recent <a href="https://msdn.microsoft.com/bafaf206-cc53-4537-b7a5-2903fbfca893">ClipCursor</a> function call, the system automatically adjusts the coordinates so that the cursor stays within the rectangle. 


## -parameters




### -param X [in]

Type: <b>int</b>

The new x-coordinate of the cursor, in screen coordinates. 


### -param Y [in]

Type: <b>int</b>

The new y-coordinate of the cursor, in screen coordinates. 


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful or zero otherwise. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The cursor is a shared resource. A window should move the cursor only when the cursor is in the window's client area.

The calling process must have <b>WINSTA_WRITEATTRIBUTES</b> access to the window station.

The input desktop must be the current desktop when you call <b>SetCursorPos</b>. Call <a href="https://msdn.microsoft.com/023d421e-bf32-4e08-b5b3-b7b2ca6c4e00">OpenInputDesktop</a> to determine whether the current desktop is the input desktop. If it is not, call <a href="https://msdn.microsoft.com/619c591f-54b7-4b61-aa07-fc57e05ee37a">SetThreadDesktop</a> with the <b>HDESK</b> returned by <b>OpenInputDesktop</b> to switch to that desktop.


#### Examples

For an example, see <a href="using_cursors.htm">Using the Keyboard to Move the Cursor</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bafaf206-cc53-4537-b7a5-2903fbfca893">ClipCursor</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/c76370d3-741a-4192-97d4-d63d2885b36b">GetCursorPos</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0a8d4ca6-d409-4468-b29a-552adbea0918">SetCaretPos</a>



<a href="https://msdn.microsoft.com/69bb9f90-5366-4141-97b6-57e41b774614">SetCursor</a>



<a href="https://msdn.microsoft.com/6712b6b7-bdb0-4078-ba38-7ad744bbf765">ShowCursor</a>
 

 

