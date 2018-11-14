---
UID: NF:comsvcs.IHolder.TrackResource
title: IHolder::TrackResource
author: windows-sdk-content
description: Tracks the resource.
old-location: cos\iholder_trackresource.htm
tech.root: cossdk
ms.assetid: 8c87727a-fefd-4ef6-964c-3379d22178c2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IHolder interface [COM+],TrackResource method, IHolder.TrackResource, IHolder::TrackResource, TrackResource, TrackResource method [COM+], TrackResource method [COM+],IHolder interface, _dtc_IHolder_TrackResource, comsvcs/IHolder::TrackResource, cos.iholder_trackresource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IHolder.TrackResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IHolder.TrackResource
: 
---

# IHolder::TrackResource


## -description


Tracks the resource.


## -parameters




### -param __MIDL__IHolder0003

TBD




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
 

 

