---
UID: NF:winuser.GetPhysicalCursorPos
title: GetPhysicalCursorPos function
author: windows-sdk-content
description: Retrieves the position of the cursor in physical coordinates.
old-location: menurc\getphysicalcursorpos.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getphysicalcursorpos.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetPhysicalCursorPos, GetPhysicalCursorPos function [Menus and Other Resources], _win32_GetPhysicalCursorPos, _win32_getphysicalcursorpos_cpp, menurc.getphysicalcursorpos, winui._win32_getphysicalcursorpos, winuser/GetPhysicalCursorPos
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - GetPhysicalCursorPos
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



For a description of the difference between logicial coordinates and physical coordinates, see <a href="https://msdn.microsoft.com/en-us/library/ms633536(v=VS.85).aspx">PhysicalToLogicalPoint</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648383(v=VS.85).aspx">ClipCursor</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646970(v=VS.85).aspx">Cursors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648390(v=VS.85).aspx">GetCursorPos</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648405(v=VS.85).aspx">SetCaretPos</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648393(v=VS.85).aspx">SetCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648394(v=VS.85).aspx">SetCursorPos</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa969465(v=VS.85).aspx">SetPhysicalCursorPos</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648396(v=VS.85).aspx">ShowCursor</a>
 

 

