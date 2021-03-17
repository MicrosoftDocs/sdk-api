---
UID: NF:comsvcs.IServiceTransactionConfigBase.ConfigureTransaction
title: IServiceTransactionConfigBase::ConfigureTransaction (comsvcs.h)
description: Configures how transactions are used in the enclosed work.
helpviewer_keywords: ["ConfigureTransaction","ConfigureTransaction method [COM+]","ConfigureTransaction method [COM+]","IServiceTransactionConfigBase interface","IServiceTransactionConfigBase interface [COM+]","ConfigureTransaction method","IServiceTransactionConfigBase.ConfigureTransaction","IServiceTransactionConfigBase::ConfigureTransaction","_cos_IServiceTransactionConfigBase_ConfigureTransaction","comsvcs/IServiceTransactionConfigBase::ConfigureTransaction","cos.iservicetransactionconfigbase_configuretransaction"]
old-location: cos\iservicetransactionconfigbase_configuretransaction.htm
tech.root: cos
ms.assetid: 8277b133-2c0c-4a21-b441-457efb285178
ms.date: 12/05/2018
ms.keywords: ConfigureTransaction, ConfigureTransaction method [COM+], ConfigureTransaction method [COM+],IServiceTransactionConfigBase interface, IServiceTransactionConfigBase interface [COM+],ConfigureTransaction method, IServiceTransactionConfigBase.ConfigureTransaction, IServiceTransactionConfigBase::ConfigureTransaction, _cos_IServiceTransactionConfigBase_ConfigureTransaction, comsvcs/IServiceTransactionConfigBase::ConfigureTransaction, cos.iservicetransactionconfigbase_configuretransaction
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
 - IServiceTransactionConfigBase::ConfigureTransaction
 - comsvcs/IServiceTransactionConfigBase::ConfigureTransaction
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
 - IServiceTransactionConfigBase.ConfigureTransaction
---

# IServiceTransactionConfigBase::ConfigureTransaction


## -description

Configures how transactions are used in the enclosed work.

## -parameters

### -param transactionConfig [in]

A value from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_transactionconfig">CSC_TransactionConfig</a> enumeration.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfigbase">IServiceTransactionConfigBase</a>