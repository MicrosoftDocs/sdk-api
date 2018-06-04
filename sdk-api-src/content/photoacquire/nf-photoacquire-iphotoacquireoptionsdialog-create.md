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

# IPhotoAcquireOptionsDialog::Create


## -description



The <code>Create</code> method creates and displays a modeless instance of the photo options dialog box, hosted within a parent window.




## -parameters




### -param hWndParent [in]

Handle to the parent window.


### -param phWndDialog [out]

Specifies the created dialog box.


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



The <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method should be called prior to the <code>Create</code> method.

The parent window indicated by <i>hWndParent</i> provides <b>OK</b> and <b>Cancel</b> buttons to the new dialog box instance.




## -see-also




<a href="https://msdn.microsoft.com/075e188f-e533-403d-be06-6a3260479f1a">IPhotoAcquireOptionsDialog Interface</a>
 

 

