---
UID: NF:comsvcs.IServicePoolConfig.put_TransactionAffinity
title: IServicePoolConfig::put_TransactionAffinity (comsvcs.h)
description: Sets whether objects involved in transactions are held until the transaction completes.
helpviewer_keywords: ["IServicePoolConfig interface [COM+]","put_TransactionAffinity method","IServicePoolConfig.put_TransactionAffinity","IServicePoolConfig::put_TransactionAffinity","comsvcs/IServicePoolConfig::put_TransactionAffinity","cos.iservicepoolconfig_put_transactionaffinity","put_TransactionAffinity","put_TransactionAffinity method [COM+]","put_TransactionAffinity method [COM+]","IServicePoolConfig interface"]
old-location: cos\iservicepoolconfig_put_transactionaffinity.htm
tech.root: cos
ms.assetid: 2f69bae2-560d-455b-b1b4-922c2fb4563a
ms.date: 12/05/2018
ms.keywords: IServicePoolConfig interface [COM+],put_TransactionAffinity method, IServicePoolConfig.put_TransactionAffinity, IServicePoolConfig::put_TransactionAffinity, comsvcs/IServicePoolConfig::put_TransactionAffinity, cos.iservicepoolconfig_put_transactionaffinity, put_TransactionAffinity, put_TransactionAffinity method [COM+], put_TransactionAffinity method [COM+],IServicePoolConfig interface
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
 - IServicePoolConfig::put_TransactionAffinity
 - comsvcs/IServicePoolConfig::put_TransactionAffinity
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
 - IServicePoolConfig.put_TransactionAffinity
---

# IServicePoolConfig::put_TransactionAffinity


## -description

Sets whether objects involved in transactions are held until the transaction completes.

## -parameters

### -param fTxAffinity [in]

<b>TRUE</b> if the objects are to be held and <b>FALSE</b> otherwise.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepoolconfig">IServicePoolConfig</a>