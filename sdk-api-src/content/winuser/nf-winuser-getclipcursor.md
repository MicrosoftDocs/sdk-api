---
UID: NF:winuser.GetClipCursor
title: GetClipCursor function
author: windows-sdk-content
description: Retrieves the screen coordinates of the rectangular area to which the cursor is confined.
old-location: menurc\getclipcursor.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getclipcursor.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetClipCursor, GetClipCursor function [Menus and Other Resources], _win32_GetClipCursor, _win32_getclipcursor_cpp, menurc.getclipcursor, winui._win32_getclipcursor, winuser/GetClipCursor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-RTCore-NTUser-Cursor-L1-1-0.dll
 - MinUser.dll
api_name:
 - GetClipCursor
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetClipCursor function


## -description


Retrieves the screen coordinates of the rectangular area to which the cursor is confined. 


## -parameters




### -param lpRect [out]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that receives the screen coordinates of the confining rectangle. The structure receives the dimensions of the screen if the cursor is not confined to a rectangle. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The cursor is a shared resource. If an application confines the cursor with the <a href="https://msdn.microsoft.com/en-us/library/ms648383(v=VS.85).aspx">ClipCursor</a> function, it must later release the cursor by using <b>ClipCursor</b> before relinquishing control to another application. 

The calling process must have <b>WINSTA_READATTRIBUTES</b> access to the window station. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms648380(v=VS.85).aspx">Confining a Cursor</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648383(v=VS.85).aspx">ClipCursor</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646970(v=VS.85).aspx">Cursors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648390(v=VS.85).aspx">GetCursorPos</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<b>Reference</b>
 

 

