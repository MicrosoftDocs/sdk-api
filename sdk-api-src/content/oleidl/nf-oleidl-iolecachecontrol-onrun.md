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

# IOleCacheControl::OnRun


## -description


Notifies the cache that the data source object has entered the running state so that the cache object can establish advise sinks as needed.


## -parameters




### -param pDataObject [in]

A pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the object that is entering the running state.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the  arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available for this operation.

</td>
</tr>
</table>
 




## -remarks



When <b>OnRun</b> is called, the cache sets up advisory connections as necessary with the source data object so it can receive notifications. The advisory connection created between the running object and the cache is destroyed when <a href="https://msdn.microsoft.com/95e62e9d-39bd-4bf8-ba25-c6a9c7fc515b">IOleCacheControl::OnStop</a> is called.

Some object handlers or in-process servers might use the cache passively, and not call <b>OnRun</b>. These applications must call <a href="https://msdn.microsoft.com/67bb0bcf-981a-4b2f-8ab9-2afc0659b2db">IOleCache2::UpdateCache</a>, <a href="https://msdn.microsoft.com/4b1f2fb6-636c-47dd-8f89-884f7b4f3977">IOleCache::InitCache</a>, or <a href="https://msdn.microsoft.com/b826411d-6e00-44ba-8603-85db40c4a55f">IOleCache::SetData</a> to fill the cache when necessary to ensure that the cache gets updated.

<b>OnRun</b> does not add a reference count on the pointer to <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> passed in <i>pDataObject</i>. Because it is the responsibility of the caller of <a href="https://msdn.microsoft.com/9035f996-b163-4855-aa9d-184b77072ead">OleRun</a> to ensure that the lifetime of the <i>pDataObject</i> pointer lasts until <a href="https://msdn.microsoft.com/95e62e9d-39bd-4bf8-ba25-c6a9c7fc515b">OnStop</a> is called, the caller must be holding a pointer to <b>IDataObject</b> on the data object of interest.




## -see-also




<a href="https://msdn.microsoft.com/67bb0bcf-981a-4b2f-8ab9-2afc0659b2db">IOleCache2::UpdateCache</a>



<a href="https://msdn.microsoft.com/64cc7a29-0bbb-4535-a7b5-9b1d82ad7e8a">IOleCacheControl</a>



<a href="https://msdn.microsoft.com/95e62e9d-39bd-4bf8-ba25-c6a9c7fc515b">IOleCacheControl::OnStop</a>
 

 

