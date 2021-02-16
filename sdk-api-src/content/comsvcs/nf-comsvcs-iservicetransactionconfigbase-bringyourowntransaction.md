---
UID: NF:comsvcs.IServiceTransactionConfigBase.BringYourOwnTransaction
title: IServiceTransactionConfigBase::BringYourOwnTransaction (comsvcs.h)
description: Enables you to run the enclosed code in an existing transaction that you provide.
helpviewer_keywords: ["BringYourOwnTransaction","BringYourOwnTransaction method [COM+]","BringYourOwnTransaction method [COM+]","IServiceTransactionConfigBase interface","IServiceTransactionConfigBase interface [COM+]","BringYourOwnTransaction method","IServiceTransactionConfigBase.BringYourOwnTransaction","IServiceTransactionConfigBase::BringYourOwnTransaction","_cos_IServiceTransactionConfigBase_BringYourOwnTransaction","comsvcs/IServiceTransactionConfigBase::BringYourOwnTransaction","cos.iservicetransactionconfigbase_bringyourowntransaction"]
old-location: cos\iservicetransactionconfigbase_bringyourowntransaction.htm
tech.root: cos
ms.assetid: fcd65d90-8855-41e9-a22d-d2b1d46e98fa
ms.date: 12/05/2018
ms.keywords: BringYourOwnTransaction, BringYourOwnTransaction method [COM+], BringYourOwnTransaction method [COM+],IServiceTransactionConfigBase interface, IServiceTransactionConfigBase interface [COM+],BringYourOwnTransaction method, IServiceTransactionConfigBase.BringYourOwnTransaction, IServiceTransactionConfigBase::BringYourOwnTransaction, _cos_IServiceTransactionConfigBase_BringYourOwnTransaction, comsvcs/IServiceTransactionConfigBase::BringYourOwnTransaction, cos.iservicetransactionconfigbase_bringyourowntransaction
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
 - IServiceTransactionConfigBase::BringYourOwnTransaction
 - comsvcs/IServiceTransactionConfigBase::BringYourOwnTransaction
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
 - IServiceTransactionConfigBase.BringYourOwnTransaction
---

# IServiceTransactionConfigBase::BringYourOwnTransaction


## -description

Enables you to run the enclosed code in an existing transaction that you provide.

## -parameters

### -param szTipURL [in]

The Transaction Internet Protocol (TIP) URL of the existing transaction in which you want to run the enclosed code.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

When you bring your own transaction, that transaction's settings override the settings from the inherited methods of the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfigbase">IServiceTransactionConfigBase</a> interface.

The <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicetransactionconfig-configurebyot">IServiceTransactionConfig::ConfigureBYOT</a> and the <b>BringYourOwnTransaction</b> methods are identical in behavior; the only difference is the type of parameter passed to each method.

## -see-also

<a href="/windows/desktop/cossdk/bring-your-own-transaction--byot-">Bring Your Own Transaction (BYOT)</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfigbase">IServiceTransactionConfigBase</a>