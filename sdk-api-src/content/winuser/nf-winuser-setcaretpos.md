---
UID: NF:winuser.SetCaretPos
title: SetCaretPos function
author: windows-sdk-content
description: Moves the caret to the specified coordinates. If the window that owns the caret was created with the CS_OWNDC class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window.
old-location: menurc\setcaretpos.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\setcaretpos.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetCaretPos, SetCaretPos function [Menus and Other Resources], _win32_SetCaretPos, _win32_setcaretpos_cpp, menurc.setcaretpos, winui._win32_setcaretpos, winuser/SetCaretPos
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
 - Ext-MS-Win-NTUser-caret-l1-1-0.dll
 - api-ms-win-ntuser-ie-caret-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - SetCaretPos
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetCaretPos function


## -description


Moves the caret to the specified coordinates. If the window that owns the caret was created with the <b>CS_OWNDC</b> class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window. 


## -parameters




### -param X [in]

Type: <b>int</b>

The new x-coordinate of the caret. 


### -param Y [in]

Type: <b>int</b>

The new y-coordinate of the caret. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>SetCaretPos</b> moves the caret whether the caret is hidden. 

The system provides one caret per queue. A window should create a caret only when it has the keyboard focus or is active. The window should destroy the caret before losing the keyboard focus or becoming inactive. A window can set the caret position only if it owns the caret. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The provided position is interpreted as logical coordinates in terms of the window associated with the caret. The calling thread is not taken into consideration.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms648398(v=VS.85).aspx">Creating and Displaying a Caret</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646968(v=VS.85).aspx">Carets</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648402(v=VS.85).aspx">GetCaretPos</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648403(v=VS.85).aspx">HideCaret</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648406(v=VS.85).aspx">ShowCaret</a>
 

 

