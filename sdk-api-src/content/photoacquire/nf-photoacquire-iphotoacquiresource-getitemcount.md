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

# IPhotoAcquireSource::GetItemCount


## -description



The <code>GetItemCount</code> method retrieves the number of items found by the <a href="https://msdn.microsoft.com/1e0ebbc7-888d-4044-8257-47c1719cf7fc">InitializeItemList</a> method.




## -parameters




### -param pnItemCount [out]

Pointer to an integer value containing the item count.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed where a non-NULL pointer was expected.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, call <a href="https://msdn.microsoft.com/1e0ebbc7-888d-4044-8257-47c1719cf7fc">InitializeItemList</a> to initialize the item list.




## -see-also




<a href="https://msdn.microsoft.com/6671d550-8c12-40e3-bf6f-33203e69cff0">IPhotoAcquireSource Interface</a>



<a href="https://msdn.microsoft.com/1e0ebbc7-888d-4044-8257-47c1719cf7fc">IPhotoAcquireSource::InitializeItemList</a>
 

 

