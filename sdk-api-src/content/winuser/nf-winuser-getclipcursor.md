---
UID: NF:winuser.GetClipCursor
title: GetClipCursor function
author: windows-sdk-content
description: Retrieves the screen coordinates of the rectangular area to which the cursor is confined.
old-location: menurc\getclipcursor.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getclipcursor.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetClipCursor, GetClipCursor function [Menus and Other Resources], _win32_GetClipCursor, _win32_getclipcursor_cpp, menurc.getclipcursor, winui._win32_getclipcursor, winuser/GetClipCursor
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	ext-ms-win-ntuser-gui-l1-2-1.dll
-	Ext-MS-Win-RTCore-NTUser-Cursor-L1-1-0.dll
-	MinUser.dll
api_name:
-	GetClipCursor
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

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the screen coordinates of the confining rectangle. The structure receives the dimensions of the screen if the cursor is not confined to a rectangle. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The cursor is a shared resource. If an application confines the cursor with the <a href="https://msdn.microsoft.com/bafaf206-cc53-4537-b7a5-2903fbfca893">ClipCursor</a> function, it must later release the cursor by using <b>ClipCursor</b> before relinquishing control to another application. 

The calling process must have <b>WINSTA_READATTRIBUTES</b> access to the window station. 


#### Examples

For an example, see <a href="using_cursors.htm">Confining a Cursor</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bafaf206-cc53-4537-b7a5-2903fbfca893">ClipCursor</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/c76370d3-741a-4192-97d4-d63d2885b36b">GetCursorPos</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<b>Reference</b>
 

 

