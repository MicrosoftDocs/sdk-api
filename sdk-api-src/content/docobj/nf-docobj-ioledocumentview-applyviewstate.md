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

# IOleDocumentView::ApplyViewState


## -description


Initializes a view with view state previously saved in call to <a href="https://msdn.microsoft.com/d270b441-d0d5-4dd5-995b-6ca5738747c5">IOleDocumentView::SaveViewState</a>.


## -parameters




### -param pstm [in]

A pointer to a stream containing data from which the view should initialize itself.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>pstm</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This view has no meaningful state to load. This error should be rare because most views will have at least some state information worth loading.

</td>
</tr>
</table>
 




## -remarks



Typically, this function is called after an existing view has been created in the container but before that view has been displayed. It is the responsibility of the view to validate the data in the view stream; the container does not attempt to interpret the view's state data.




## -see-also




<a href="https://msdn.microsoft.com/709d7ff4-d32d-405f-8839-b05df49ef751">IOleDocument::CreateView</a>



<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>



<a href="https://msdn.microsoft.com/d270b441-d0d5-4dd5-995b-6ca5738747c5">IOleDocumentView::SaveViewState</a>
 

 

