---
UID: NF:comsvcs.IHolder.FreeResource
title: IHolder::FreeResource (comsvcs.h)
description: Returns a resource to the inventory.
helpviewer_keywords: ["FreeResource","FreeResource method [COM+]","FreeResource method [COM+]","IHolder interface","IHolder interface [COM+]","FreeResource method","IHolder.FreeResource","IHolder::FreeResource","_dtc_IHolder_FreeResource","comsvcs/IHolder::FreeResource","cos.iholder_freeresource"]
old-location: cos\iholder_freeresource.htm
tech.root: cos
ms.assetid: 1d110bf6-7204-4fbb-abb7-ced7cf885e5b
ms.date: 12/05/2018
ms.keywords: FreeResource, FreeResource method [COM+], FreeResource method [COM+],IHolder interface, IHolder interface [COM+],FreeResource method, IHolder.FreeResource, IHolder::FreeResource, _dtc_IHolder_FreeResource, comsvcs/IHolder::FreeResource, cos.iholder_freeresource
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
 - IHolder::FreeResource
 - comsvcs/IHolder::FreeResource
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
 - IHolder.FreeResource
---

# IHolder::FreeResource


## -description

Returns a resource to the inventory.

## -parameters

### -param __MIDL__IHolder0002 [in]

The handle of the resource to be freed.

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
<i>ResTypId</i> is not a valid resource handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL </b></dt>
</dl>
</td>
<td width="60%">
The method failed. The resource has not been freed.

</td>
</tr>
</table>

## -remarks

A resource originally returned by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iholder-allocresource">IHolder::AllocResource</a> is returned to the pool. This notifies the Resource Dispenser through <a href="/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-resetresource">IDispenserDriver::ResetResource</a>, which is the Resource Dispenser's opportunity to prepare the resource before it is returned to the pool.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iholder">IHolder</a>