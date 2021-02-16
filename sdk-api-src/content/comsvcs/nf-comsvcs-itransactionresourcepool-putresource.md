---
UID: NF:comsvcs.ITransactionResourcePool.PutResource
title: ITransactionResourcePool::PutResource (comsvcs.h)
description: Adds an object to the list of pooled objects.
helpviewer_keywords: ["ITransactionResourcePool interface [COM+]","PutResource method","ITransactionResourcePool.PutResource","ITransactionResourcePool::PutResource","PutResource","PutResource method [COM+]","PutResource method [COM+]","ITransactionResourcePool interface","_cos_ITransactionResourcePool_PutResource","comsvcs/ITransactionResourcePool::PutResource","cos.itransactionresourcepool_putresource"]
old-location: cos\itransactionresourcepool_putresource.htm
tech.root: cos
ms.assetid: 6e05f075-0fa8-4605-9f68-3ef7fc9f0132
ms.date: 12/05/2018
ms.keywords: ITransactionResourcePool interface [COM+],PutResource method, ITransactionResourcePool.PutResource, ITransactionResourcePool::PutResource, PutResource, PutResource method [COM+], PutResource method [COM+],ITransactionResourcePool interface, _cos_ITransactionResourcePool_PutResource, comsvcs/ITransactionResourcePool::PutResource, cos.itransactionresourcepool_putresource
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
 - ITransactionResourcePool::PutResource
 - comsvcs/ITransactionResourcePool::PutResource
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
 - ITransactionResourcePool.PutResource
---

# ITransactionResourcePool::PutResource


## -description

Adds an object to the list of pooled objects.

## -parameters

### -param pPool [in]

The key to each object in the transaction resource pool. It determines the type of pooled object to add to the list.

### -param pUnk [in]

A reference to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the pooled object.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjpool">IObjPool</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionresourcepool">ITransactionResourcePool</a>