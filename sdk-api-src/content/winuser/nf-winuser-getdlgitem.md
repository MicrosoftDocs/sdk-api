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

# GetDlgItem function


## -description


Retrieves a handle to a control in the specified dialog box. 


## -parameters




### -param hDlg [in, optional]

Type: <b>HWND</b>

A handle to the dialog box that contains the control. 


### -param nIDDlgItem [in]

Type: <b>int</b>

The identifier of the control to be retrieved. 


## -returns



Type: <b>HWND</b>

If the function succeeds, the return value is the window handle of the specified control. 

If the function fails, the return value is <b>NULL</b>, indicating an invalid dialog box handle or a nonexistent control. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You can use the <b>GetDlgItem</b> function with any parent-child window pair, not just with dialog boxes. As long as the <i>hDlg</i> parameter specifies a parent window and the child window has a unique identifier (as specified by the <i>hMenu</i> parameter in the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> or <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function that created the child window), <b>GetDlgItem</b> returns a valid handle to the child window. 


#### Examples


			
			For an example, see <a href="using_dialog_boxes.htm">Initializing a Dialog Box</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/07ebee3c-5aa7-4b0d-b6cb-e642e01e1a88">Dialog Boxes</a>



<a href="https://msdn.microsoft.com/8a0b8275-35e5-4983-9b2d-968023d39aa3">GetDlgItemInt</a>



<a href="https://msdn.microsoft.com/6cfaa693-aafe-4034-abcb-0a8364cccb4b">GetDlgItemText</a>



<b>Reference</b>
 

 

