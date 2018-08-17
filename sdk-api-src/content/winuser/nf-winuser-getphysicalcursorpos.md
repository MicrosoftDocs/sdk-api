---
UID: NF:winuser.GetPhysicalCursorPos
title: GetPhysicalCursorPos function
author: windows-sdk-content
description: Retrieves the position of the cursor in physical coordinates.
old-location: menurc\getphysicalcursorpos.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getphysicalcursorpos.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPhysicalCursorPos, GetPhysicalCursorPos function [Menus and Other Resources], _win32_GetPhysicalCursorPos, _win32_getphysicalcursorpos_cpp, menurc.getphysicalcursorpos, winui._win32_getphysicalcursorpos, winuser/GetPhysicalCursorPos
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - GetPhysicalCursorPos
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetPhysicalCursorPos function


## -description


Retrieves the position of the cursor in physical coordinates.


## -parameters




### -param lpPoint [out]

Type: <b>LPPOINT</b>

The position of the cursor, in physical coordinates.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise <b>FALSE</b>.


<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be called to get more information about any error that is generated.




## -remarks



For a description of the difference between logicial coordinates and physical coordinates, see <a href="https://msdn.microsoft.com/7b02d31f-f1c7-4be1-817d-f7cc6850008d">PhysicalToLogicalPoint</a>.




## -see-also




<a href="https://msdn.microsoft.com/bafaf206-cc53-4537-b7a5-2903fbfca893">ClipCursor</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/c76370d3-741a-4192-97d4-d63d2885b36b">GetCursorPos</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0a8d4ca6-d409-4468-b29a-552adbea0918">SetCaretPos</a>



<a href="https://msdn.microsoft.com/69bb9f90-5366-4141-97b6-57e41b774614">SetCursor</a>



<a href="https://msdn.microsoft.com/b17cf57f-dd96-4695-a51e-ee1e1f00f85f">SetCursorPos</a>



<a href="https://msdn.microsoft.com/6f5252f4-fa6f-4f0d-9150-cc31e01f83f2">SetPhysicalCursorPos</a>



<a href="https://msdn.microsoft.com/6712b6b7-bdb0-4078-ba38-7ad744bbf765">ShowCursor</a>
 

 

