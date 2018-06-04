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

# GetDlgCtrlID function


## -description


Retrieves the identifier of the specified control. 


## -parameters




### -param hWnd

TBD




#### - hwndCtl [in]

Type: <b>HWND</b>

A handle to the control. 


## -returns



Type: <b>int</b>

If the function succeeds, the return value is the identifier of the control.

If the function fails, the return value is zero. An invalid value for the <i>hwndCtl</i> parameter, for example, will cause the function to fail. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>GetDlgCtrlID</b> accepts child window handles as well as handles of controls in dialog boxes. An application sets the identifier for a child window when it creates the window by assigning the identifier value to the <i>hmenu</i> parameter when calling the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> or <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function. 

Although <b>GetDlgCtrlID</b> may return a value if <i>hwndCtl</i> is a handle to a top-level window, top-level windows cannot have identifiers and such a return value is never valid. 


#### Examples


			
			For an example, see <a href="using_dialog_boxes.htm">Initializing a Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/c119d716-b07f-4644-9d51-da94fab3e516">GetDlgItem</a>



<b>Reference</b>
 

 

