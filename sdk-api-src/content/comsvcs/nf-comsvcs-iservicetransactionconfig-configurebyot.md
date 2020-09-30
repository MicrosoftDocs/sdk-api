---
UID: NF:comsvcs.IServiceTransactionConfig.ConfigureBYOT
title: IServiceTransactionConfig::ConfigureBYOT (comsvcs.h)
description: Enables you to configure the transaction that you use when you bring your own transaction.
helpviewer_keywords: ["ConfigureBYOT","ConfigureBYOT method [COM+]","ConfigureBYOT method [COM+]","IServiceTransactionConfig interface","IServiceTransactionConfig interface [COM+]","ConfigureBYOT method","IServiceTransactionConfig.ConfigureBYOT","IServiceTransactionConfig::ConfigureBYOT","_cos_IServiceTransactionConfig_ConfigureBYOT","comsvcs/IServiceTransactionConfig::ConfigureBYOT","cos.iservicetransactionconfig_configurebyot"]
old-location: cos\iservicetransactionconfig_configurebyot.htm
tech.root: cos
ms.assetid: be4fa727-962e-4254-8615-58f6ced15fc3
ms.date: 12/05/2018
ms.keywords: ConfigureBYOT, ConfigureBYOT method [COM+], ConfigureBYOT method [COM+],IServiceTransactionConfig interface, IServiceTransactionConfig interface [COM+],ConfigureBYOT method, IServiceTransactionConfig.ConfigureBYOT, IServiceTransactionConfig::ConfigureBYOT, _cos_IServiceTransactionConfig_ConfigureBYOT, comsvcs/IServiceTransactionConfig::ConfigureBYOT, cos.iservicetransactionconfig_configurebyot
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
 - IServiceTransactionConfig::ConfigureBYOT
 - comsvcs/IServiceTransactionConfig::ConfigureBYOT
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
 - IServiceTransactionConfig.ConfigureBYOT
---

# IServiceTransactionConfig::ConfigureBYOT


## -description

Enables you to configure the transaction that you use when you bring your own transaction.

## -parameters

### -param pITxByot [in]

A pointer to the <b>ITransaction</b> interface of the existing transaction in which you want to run the enclosed code.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

When you bring your own transaction, that transaction's settings override the settings from the inherited methods of the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfig">IServiceTransactionConfig</a> interface.

The <b>ConfigureBYOT</b> and the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicetransactionconfigbase-bringyourowntransaction">IServiceTransactionConfigBase::BringYourOwnTransaction</a> methods are identical in behavior; the only difference is the type of parameter passed to each method.

## -see-also

<a href="/windows/desktop/cossdk/bring-your-own-transaction--byot-">Bring Your Own Transaction (BYOT)</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfig">IServiceTransactionConfig</a>