---
UID: NF:winuser.ShowCursor
title: ShowCursor function
author: windows-sdk-content
description: Displays or hides the cursor.
old-location: menurc\showcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\showcursor.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ShowCursor, ShowCursor function [Menus and Other Resources], _win32_ShowCursor, _win32_showcursor_cpp, menurc.showcursor, winui._win32_showcursor, winuser/ShowCursor
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
 - Ext-MS-Win-Ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-RTCore-NTUser-Cursor-L1-1-0.dll
 - MinUser.dll
api_name:
 - ShowCursor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ShowCursor
: 
---

# ShowCursor function


## -description


Displays or hides the cursor. 


## -parameters




### -param bShow [in]

Type: <b>BOOL</b>

If <i>bShow</i> is <b>TRUE</b>, the display count is incremented by one. If <i>bShow</i> is <b>FALSE</b>, the display count is decremented by one. 


## -returns



Type: <b>int</b>

The return value specifies the new display counter.




## -remarks



<b>Windows 8</b>: Call <a href="https://msdn.microsoft.com/en-us/library/ms648389(v=VS.85).aspx">GetCursorInfo</a> to determine the cursor visibility.

This function sets an internal display counter that determines whether the cursor should be displayed. The cursor is displayed only if the display count is greater than or equal to 0. If a mouse is installed, the initial display count is 0. If no mouse is installed, the display count is 
				–1.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648383(v=VS.85).aspx">ClipCursor</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646970(v=VS.85).aspx">Cursors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648390(v=VS.85).aspx">GetCursorPos</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648393(v=VS.85).aspx">SetCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648394(v=VS.85).aspx">SetCursorPos</a>
 

 

