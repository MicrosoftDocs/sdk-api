---
UID: NF:comsvcs.IHolder.TrackResource
title: IHolder::TrackResource (comsvcs.h)
description: Tracks the resource.
helpviewer_keywords: ["IHolder interface [COM+]","TrackResource method","IHolder.TrackResource","IHolder::TrackResource","TrackResource","TrackResource method [COM+]","TrackResource method [COM+]","IHolder interface","_dtc_IHolder_TrackResource","comsvcs/IHolder::TrackResource","cos.iholder_trackresource"]
old-location: cos\iholder_trackresource.htm
tech.root: cos
ms.assetid: 8c87727a-fefd-4ef6-964c-3379d22178c2
ms.date: 12/05/2018
ms.keywords: IHolder interface [COM+],TrackResource method, IHolder.TrackResource, IHolder::TrackResource, TrackResource, TrackResource method [COM+], TrackResource method [COM+],IHolder interface, _dtc_IHolder_TrackResource, comsvcs/IHolder::TrackResource, cos.iholder_trackresource
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IHolder::TrackResource
 - comsvcs/IHolder::TrackResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IHolder.TrackResource
---

# IHolder::TrackResource


## -description

Tracks the resource.

## -parameters

### -param __MIDL__IHolder0003 [in]

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

TrackResource tells the Holder that a resource should be tracked until it is freed by calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iholder-untrackresource">IHolder::UntrackResource</a>, or until the object that called <b>TrackResource</b> is released, at which time the Dispenser Manager automatically frees the resource.

If <b>TrackResource</b> is called from a transactional object, it calls back to the Resource Dispenser's <a href="/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-enlistresource">IDispenserDriver::EnlistResource</a> method. The <b>EnlistResource</b> method can enlist the resource in the transaction, or it can return S_FALSE, indicating that the resource is not transaction capable and has not been enlisted.

This resource is eventually destroyed after both of the following are true: 



<ul>
<li>The Resource Dispenser calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iholder-untrackresource">IHolder::UntrackResource</a> (most likely at the component's request), or the object's lifetime ends.</li>
<li>The transaction that the resource was enlisted in (if any) is done.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iholder">IHolder</a>