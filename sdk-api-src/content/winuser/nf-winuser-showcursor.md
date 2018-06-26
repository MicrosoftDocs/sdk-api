---
UID: NF:winuser.ShowCursor
title: ShowCursor function
author: windows-sdk-content
description: Displays or hides the cursor.
old-location: menurc\showcursor.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\showcursor.htm
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ShowCursor, ShowCursor function [Menus and Other Resources], _win32_ShowCursor, _win32_showcursor_cpp, menurc.showcursor, winui._win32_showcursor, winuser/ShowCursor
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
 - Ext-MS-Win-Ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-RTCore-NTUser-Cursor-L1-1-0.dll
 - MinUser.dll
api_name:
 - ShowCursor
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



<b>Windows 8</b>: Call <a href="https://msdn.microsoft.com/4dea42e7-f78f-4e34-9e1d-e76123a209fc">GetCursorInfo</a> to determine the cursor visibility.

This function sets an internal display counter that determines whether the cursor should be displayed. The cursor is displayed only if the display count is greater than or equal to 0. If a mouse is installed, the initial display count is 0. If no mouse is installed, the display count is 
				–1.




## -see-also




<a href="https://msdn.microsoft.com/bafaf206-cc53-4537-b7a5-2903fbfca893">ClipCursor</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/c76370d3-741a-4192-97d4-d63d2885b36b">GetCursorPos</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/69bb9f90-5366-4141-97b6-57e41b774614">SetCursor</a>



<a href="https://msdn.microsoft.com/b17cf57f-dd96-4695-a51e-ee1e1f00f85f">SetCursorPos</a>
 

 

