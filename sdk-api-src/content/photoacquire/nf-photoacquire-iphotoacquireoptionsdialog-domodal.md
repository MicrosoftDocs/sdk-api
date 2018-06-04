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

# IPhotoAcquireOptionsDialog::DoModal


## -description



The <code>DoModal</code> method creates and displays the options dialog box as a modal dialog box.




## -parameters




### -param hWndParent [in]

Handle to the dialog's parent window.


### -param ppnReturnCode [out]

Specifies the code returned when the window is closed.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The modal dialog displayed by <b>DoModal</b> will have <b>OK</b> and <b>Cancel</b> buttons, whereas the <b>OK</b> and <b>Cancel</b> buttons of the modeless dialog displayed by <a href="https://msdn.microsoft.com/22eb58d2-f1cf-4115-a5d4-dceb1d3ba4ad">Create</a> must be provided by the parent window.




## -see-also




<a href="https://msdn.microsoft.com/075e188f-e533-403d-be06-6a3260479f1a">IPhotoAcquireOptionsDialog Interface</a>
 

 

