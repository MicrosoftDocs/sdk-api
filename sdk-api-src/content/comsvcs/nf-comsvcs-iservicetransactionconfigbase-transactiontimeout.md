---
UID: NF:comsvcs.IServiceTransactionConfigBase.TransactionTimeout
title: IServiceTransactionConfigBase::TransactionTimeout (comsvcs.h)
description: Sets the transaction time-out for a new transaction.
helpviewer_keywords: ["IServiceTransactionConfigBase interface [COM+]","TransactionTimeout method","IServiceTransactionConfigBase.TransactionTimeout","IServiceTransactionConfigBase::TransactionTimeout","TransactionTimeout","TransactionTimeout method [COM+]","TransactionTimeout method [COM+]","IServiceTransactionConfigBase interface","_cos_IServiceTransactionConfigBase_TransactionTimeout","comsvcs/IServiceTransactionConfigBase::TransactionTimeout","cos.iservicetransactionconfigbase_transactiontimeout"]
old-location: cos\iservicetransactionconfigbase_transactiontimeout.htm
tech.root: cos
ms.assetid: 87943fe9-ef88-49ae-96d0-99d1011478dc
ms.date: 12/05/2018
ms.keywords: IServiceTransactionConfigBase interface [COM+],TransactionTimeout method, IServiceTransactionConfigBase.TransactionTimeout, IServiceTransactionConfigBase::TransactionTimeout, TransactionTimeout, TransactionTimeout method [COM+], TransactionTimeout method [COM+],IServiceTransactionConfigBase interface, _cos_IServiceTransactionConfigBase_TransactionTimeout, comsvcs/IServiceTransactionConfigBase::TransactionTimeout, cos.iservicetransactionconfigbase_transactiontimeout
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
 - IServiceTransactionConfigBase::TransactionTimeout
 - comsvcs/IServiceTransactionConfigBase::TransactionTimeout
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
 - IServiceTransactionConfigBase.TransactionTimeout
---

# IServiceTransactionConfigBase::TransactionTimeout


## -description

Sets the transaction time-out for a new transaction.

## -parameters

### -param ulTimeoutSec [in]

The transaction time-out, in seconds.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

If the transaction does not either commit or abort within the transaction time-out period, the transaction must automatically abort. This method is ignored if the new context enlists as a nonroot transaction or does not use transactions.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfigbase">IServiceTransactionConfigBase</a>