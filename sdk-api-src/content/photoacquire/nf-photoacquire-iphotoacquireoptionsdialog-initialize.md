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

# IPhotoAcquireOptionsDialog::Initialize


## -description



Initializes the options dialog box and reads any saved options from the registry.




## -parameters




### -param pszRegistryRoot [in]

(optional) Pointer to a null-terminated string containing the registry root of a custom location to read the acquisition settings from. If this parameter is set to <b>NULL</b>, the default location will be used.


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



<code>Initialize</code> must be called prior to calling <a href="https://msdn.microsoft.com/22eb58d2-f1cf-4115-a5d4-dceb1d3ba4ad">Create</a> or <a href="https://msdn.microsoft.com/fbceebc3-10dd-4028-9672-1976a459cafe">DoModal</a>. Failure to do so will cause <b>Create</b> or <b>DoModal</b> to fail.

If <code>Initialize</code> is called while the options dialog box is already displayed, an error will be returned.




## -see-also




<a href="https://msdn.microsoft.com/075e188f-e533-403d-be06-6a3260479f1a">IPhotoAcquireOptionsDialog Interface</a>
 

 

