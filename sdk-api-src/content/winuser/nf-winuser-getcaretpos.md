---
UID: NF:winuser.GetCaretPos
title: GetCaretPos function
author: windows-sdk-content
description: Copies the caret's position to the specified POINT structure.
old-location: menurc\getcaretpos.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\getcaretpos.htm
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: GetCaretPos, GetCaretPos function [Menus and Other Resources], _win32_GetCaretPos, _win32_getcaretpos_cpp, menurc.getcaretpos, winui._win32_getcaretpos, winuser/GetCaretPos
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
 - Ext-MS-Win-NTUser-caret-l1-1-0.dll
 - api-ms-win-ntuser-ie-caret-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - GetCaretPos
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetCaretPos function


## -description


Copies the caret's position to the specified <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure. 


## -parameters




### -param lpPoint [out]

Type: <b>LPPOINT</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that is to receive the client coordinates of the caret. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.
                

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The caret position is always given in the client coordinates of the window that contains the caret. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The returned values are interpreted as logical sizes in terms of the window in question. The calling thread is not taken into consideration.




## -see-also




<a href="https://msdn.microsoft.com/34ff3420-a1d2-46cc-9378-4b3340bec8c8">Carets</a>



<b>Conceptual</b>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/0a8d4ca6-d409-4468-b29a-552adbea0918">SetCaretPos</a>
 

 

