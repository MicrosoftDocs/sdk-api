---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

