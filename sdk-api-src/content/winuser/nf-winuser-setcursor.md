---
UID: NF:winuser.SetCursor
title: SetCursor function
author: windows-sdk-content
description: Sets the cursor shape.
old-location: menurc\setcursor.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\setcursor.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SetCursor, SetCursor function [Menus and Other Resources], _win32_SetCursor, _win32_setcursor_cpp, menurc.setcursor, winui._win32_setcursor, winuser/SetCursor
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
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetCursor function


## -description


Sets the cursor shape. 


## -parameters




### -param hCursor [in, optional]

Type: <b>HCURSOR</b>

A handle to the cursor. The cursor must have been created by the <a href="https://msdn.microsoft.com/8a5bb069-4c2b-4924-9455-e6c91fef8461">CreateCursor</a> function or loaded by the <a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a> or <a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a> function. If this parameter is <b>NULL</b>, the cursor is removed from the screen.


## -returns



Type: <b>HCURSOR</b>

The return value is the handle to the previous cursor, if there was one. 

If there was no previous cursor, the return value is <b>NULL</b>. 




## -remarks



The cursor is set only if the new cursor is different from the previous cursor; otherwise, the function returns immediately. 

The cursor is a shared resource. A window should set the cursor shape only when the cursor is in its client area or when the window is capturing mouse input. In systems without a mouse, the window should restore the previous cursor before the cursor leaves the client area or before it relinquishes control to another window. 

If your application must set the cursor while it is in a window, make sure the class cursor for the specified window's class is set to <b>NULL</b>. If the class cursor is not <b>NULL</b>, the system restores the class cursor each time the mouse is moved. 

The cursor is not shown on the screen if the internal cursor display count is less than zero. This occurs if the application uses the <a href="https://msdn.microsoft.com/6712b6b7-bdb0-4078-ba38-7ad744bbf765">ShowCursor</a> function to hide the cursor more times than to show the cursor. 


#### Examples

For an example, see <a href="using_cursors.htm">Displaying a Cursor</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8a5bb069-4c2b-4924-9455-e6c91fef8461">CreateCursor</a>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/29ac39ae-244a-404c-9501-68c7992366a1">GetCursor</a>



<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>



<a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>



<a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/b17cf57f-dd96-4695-a51e-ee1e1f00f85f">SetCursorPos</a>



<a href="https://msdn.microsoft.com/6712b6b7-bdb0-4078-ba38-7ad744bbf765">ShowCursor</a>
 

 

