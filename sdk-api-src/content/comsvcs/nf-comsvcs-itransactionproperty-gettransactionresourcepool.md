---
UID: NF:comsvcs.ITransactionProperty.GetTransactionResourcePool
title: ITransactionProperty::GetTransactionResourcePool (comsvcs.h)
description: Retrieves the resource pool that is associated with this context's transaction.
helpviewer_keywords: ["GetTransactionResourcePool","GetTransactionResourcePool method [COM+]","GetTransactionResourcePool method [COM+]","ITransactionProperty interface","ITransactionProperty interface [COM+]","GetTransactionResourcePool method","ITransactionProperty.GetTransactionResourcePool","ITransactionProperty::GetTransactionResourcePool","_cos_ITransactionProperty_GetTransactionResourcePool","comsvcs/ITransactionProperty::GetTransactionResourcePool","cos.itransactionproperty_gettransactionresourcepool"]
old-location: cos\itransactionproperty_gettransactionresourcepool.htm
tech.root: cos
ms.assetid: 497cfbd8-122f-45c8-a34a-7e7df4932ad1
ms.date: 12/05/2018
ms.keywords: GetTransactionResourcePool, GetTransactionResourcePool method [COM+], GetTransactionResourcePool method [COM+],ITransactionProperty interface, ITransactionProperty interface [COM+],GetTransactionResourcePool method, ITransactionProperty.GetTransactionResourcePool, ITransactionProperty::GetTransactionResourcePool, _cos_ITransactionProperty_GetTransactionResourcePool, comsvcs/ITransactionProperty::GetTransactionResourcePool, cos.itransactionproperty_gettransactionresourcepool
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
 - ITransactionProperty::GetTransactionResourcePool
 - comsvcs/ITransactionProperty::GetTransactionResourcePool
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
 - ITransactionProperty.GetTransactionResourcePool
---

# ITransactionProperty::GetTransactionResourcePool


## -description

Retrieves the resource pool that is associated with this context's transaction.

## -parameters

### -param ppTxPool [out]

A reference to the transaction resource pool.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionproperty">ITransactionProperty</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionresourcepool">ITransactionResourcePool</a>