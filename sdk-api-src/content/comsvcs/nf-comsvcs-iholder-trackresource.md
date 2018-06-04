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

# IHolder::TrackResource


## -description


Tracks the resource.


## -parameters




### -param __MIDL__IHolder0003






#### - ResId [in]

The handle of the resource to be tracked. The Resource Dispenser has already created this resource before calling <b>TrackResource</b>.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ResId</i> is not a valid resource handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL </b></dt>
</dl>
</td>
<td width="60%">
The method failed. The resource has not been tracked. The likely cause is that the caller's transaction is aborting.

</td>
</tr>
</table>
 




## -remarks



Some resources are not kept in inventory; they are always manufactured on demand. The Holder is used only as a mechanism to automatically free the resources left at the end of an object's lifetime.

TrackResource tells the Holder that a resource should be tracked until it is freed by calling <a href="https://msdn.microsoft.com/380b09ad-08d6-4d25-8d80-0e56d4295b8f">IHolder::UntrackResource</a>, or until the object that called <b>TrackResource</b> is released, at which time the Dispenser Manager automatically frees the resource.

If <b>TrackResource</b> is called from a transactional object, it calls back to the Resource Dispenser's <a href="https://msdn.microsoft.com/87a8b7f4-edf3-4ab5-b75a-f8fda1f4975a">IDispenserDriver::EnlistResource</a> method. The <b>EnlistResource</b> method can enlist the resource in the transaction, or it can return S_FALSE, indicating that the resource is not transaction capable and has not been enlisted.

This resource is eventually destroyed after both of the following are true: 



<ul>
<li>The Resource Dispenser calls <a href="https://msdn.microsoft.com/380b09ad-08d6-4d25-8d80-0e56d4295b8f">IHolder::UntrackResource</a> (most likely at the component's request), or the object's lifetime ends.</li>
<li>The transaction that the resource was enlisted in (if any) is done.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/dba9c616-031d-48a7-b3e3-eb28b95a573a">IDispenserDriver</a>



<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>



<a href="https://msdn.microsoft.com/3c852e72-2fdc-4fd0-b523-f5601154da2a">IHolder</a>
 

 

