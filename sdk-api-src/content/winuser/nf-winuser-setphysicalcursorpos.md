---
UID: NF:winuser.SetPhysicalCursorPos
title: SetPhysicalCursorPos function
author: windows-sdk-content
description: Sets the position of the cursor in physical coordinates.
old-location: menurc\setphysicalcursorpos.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\setphysicalcursorpos.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetPhysicalCursorPos, SetPhysicalCursorPos function [Menus and Other Resources], _win32_SetPhysicalCursorPos, _win32_setphysicalcursorpos_cpp, menurc.setphysicalcursorpos, winui._win32_setphysicalcursorpos, winuser/SetPhysicalCursorPos
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
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
 - SetPhysicalCursorPos
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetPhysicalCursorPos function


## -description


Sets the position of the cursor in physical coordinates.


## -parameters




### -param X [in]

Type: <b>int</b>

The new x-coordinate of the cursor, in physical coordinates. 


### -param Y [in]

Type: <b>int</b>

The new y-coordinate of the cursor, in physical coordinates. 


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise <b>FALSE</b>.




## -remarks



For a description of the difference between logicial coordinates and physical coordinates, see <a href="https://msdn.microsoft.com/en-us/library/ms633536(v=VS.85).aspx">PhysicalToLogicalPoint</a>.


<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be called to get more information about any error that is generated.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648383(v=VS.85).aspx">ClipCursor</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646970(v=VS.85).aspx">Cursors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648390(v=VS.85).aspx">GetCursorPos</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa969464(v=VS.85).aspx">GetPhysicalCursorPos</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648405(v=VS.85).aspx">SetCaretPos</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648393(v=VS.85).aspx">SetCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648394(v=VS.85).aspx">SetCursorPos</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648396(v=VS.85).aspx">ShowCursor</a>
 

 

