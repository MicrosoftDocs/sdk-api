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

# IResourceConsumer::AcquireResource


## -description



The <code>AcquireResource</code> method notifies the resource consumer that a resource might be acquired.




## -parameters




### -param idResource [in]

Resource identifier of the resource to be acquired.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

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
Consumer has successfully acquired the resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Consumer has not acquired the resource but will use <a href="https://msdn.microsoft.com/a5c52f5b-1c21-4f4c-b698-15b6ec7f7fed">IResourceManager::NotifyAcquire</a> when it does.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_RESOURCE_NOT_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
Consumer no longer needs the resource.

</td>
</tr>
</table>
 

The method may return some other error code, if the consumer fails to acquire the resource.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/dda2b207-dcd8-42df-95a3-d4bfbb4a7fd8">IResourceConsumer Interface</a>
 

 

