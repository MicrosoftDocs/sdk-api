---
UID: NF:winuser.GetNextDlgTabItem
title: GetNextDlgTabItem function
author: windows-sdk-content
description: Retrieves a handle to the first control that has the WS_TABSTOP style that precedes (or follows) the specified control.
old-location: dlgbox\getnextdlgtabitem.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\dialogboxes\dialogboxreference\dialogboxfunctions\getnextdlgtabitem.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetNextDlgTabItem, GetNextDlgTabItem function [Dialog Boxes], _win32_GetNextDlgTabItem, _win32_getnextdlgtabitem_cpp, dlgbox.getnextdlgtabitem, winui._win32_getnextdlgtabitem, winuser/GetNextDlgTabItem
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
 - ext-ms-win-ntuser-dialogbox-l1-1-2.dll
api_name:
 - GetNextDlgTabItem
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetNextDlgTabItem function


## -description


Retrieves a handle to the first 
		control that has the <a href="dlgbox_programming_considerations.htm">WS_TABSTOP</a> 
		style that precedes (or follows) the specified control. 


## -parameters




### -param hDlg [in]

Type: <b>HWND</b>

A handle to the dialog box to be searched. 


### -param hCtl [in, optional]

Type: <b>HWND</b>

A handle to the control to be used as the starting point for the search. 
				If this parameter is <b>NULL</b>, the function fails. 


### -param bPrevious [in]

Type: <b>BOOL</b>

Indicates how the function is to search the dialog box. If this parameter 
				is <b>TRUE</b>, the function searches for the previous control 
				in the dialog box. If this parameter is <b>FALSE</b>, the function searches 
				for the next control in the dialog box. 


## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the window handle 
				of the previous (or next) control that has the 
				<a href="dlgbox_programming_considerations.htm">WS_TABSTOP</a> style set. 

If the function fails, the return value is <b>NULL</b>. To get extended error 
				information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>GetNextDlgTabItem</b> function searches controls in the order (or reverse order) they were created in the dialog box template. The function returns the first control it locates that is visible, not disabled, and has the <a href="dlgbox_programming_considerations.htm">WS_TABSTOP</a> style. If no such control exists, the function returns <i>hCtl</i>. 

If the search for the next control with the <b>WS_TABSTOP</b> style encounters a window with the <b>WS_EX_CONTROLPARENT</b> style, the system recursively searches the window's children.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/c119d716-b07f-4644-9d51-da94fab3e516">GetDlgItem</a>



<a href="https://msdn.microsoft.com/7677d5fa-a4bc-458c-a252-88f397407a07">GetNextDlgGroupItem</a>



<b>Reference</b>
 

 

