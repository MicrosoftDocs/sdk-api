---
UID: NF:comsvcs.ITransactionResourcePool.GetResource
title: ITransactionResourcePool::GetResource (comsvcs.h)
description: Retrieves an object from the list of pooled objects.
helpviewer_keywords: ["GetResource","GetResource method [COM+]","GetResource method [COM+]","ITransactionResourcePool interface","ITransactionResourcePool interface [COM+]","GetResource method","ITransactionResourcePool.GetResource","ITransactionResourcePool::GetResource","_cos_ITransactionResourcePool_GetResource","comsvcs/ITransactionResourcePool::GetResource","cos.itransactionresourcepool_getresource"]
old-location: cos\itransactionresourcepool_getresource.htm
tech.root: cos
ms.assetid: 68e71746-e3a1-4f33-a3b8-fa8bf9608776
ms.date: 12/05/2018
ms.keywords: GetResource, GetResource method [COM+], GetResource method [COM+],ITransactionResourcePool interface, ITransactionResourcePool interface [COM+],GetResource method, ITransactionResourcePool.GetResource, ITransactionResourcePool::GetResource, _cos_ITransactionResourcePool_GetResource, comsvcs/ITransactionResourcePool::GetResource, cos.itransactionresourcepool_getresource
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ITransactionResourcePool::GetResource
 - comsvcs/ITransactionResourcePool::GetResource
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
 - ITransactionResourcePool.GetResource
---

# ITransactionResourcePool::GetResource


## -description

Retrieves an object from the list of pooled objects.

## -parameters

### -param pPool [in]

The key to each object in the transaction resource pool. It determines the type of pooled object to retrieve from the list.

### -param ppUnk [out]

A reference to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the pooled object.

The object that is retrieved must have the same <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjpool">IObjPool</a> pointer as an object that was put on the list by using <a href="/windows/desktop/api/comsvcs/nf-comsvcs-itransactionresourcepool-putresource">PutResource</a>.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
<dt><b>E_FAILED </b></dt>
</dl>
</td>
<td width="60%">
The <i>pPool</i> parameter did not match any object on the list of pooled objects.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjpool">IObjPool</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionresourcepool">ITransactionResourcePool</a>