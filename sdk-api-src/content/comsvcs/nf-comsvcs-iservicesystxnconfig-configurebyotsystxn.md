---
UID: NF:comsvcs.IServiceSysTxnConfig.ConfigureBYOTSysTxn
title: IServiceSysTxnConfig::ConfigureBYOTSysTxn (comsvcs.h)
description: Enables you to run the enclosed code in the scope of an existing transaction that you specify with a transaction proxy.
helpviewer_keywords: ["ConfigureBYOTSysTxn","ConfigureBYOTSysTxn method [COM+]","ConfigureBYOTSysTxn method [COM+]","IServiceSysTxnConfig interface","IServiceSysTxnConfig interface [COM+]","ConfigureBYOTSysTxn method","IServiceSysTxnConfig.ConfigureBYOTSysTxn","IServiceSysTxnConfig::ConfigureBYOTSysTxn","comsvcs/IServiceSysTxnConfig::ConfigureBYOTSysTxn","cos.iservicesystxnconfig_configurebyotsystxn"]
old-location: cos\iservicesystxnconfig_configurebyotsystxn.htm
tech.root: cos
ms.assetid: 6023e756-7797-489b-96fd-9cf2d9f2cb2b
ms.date: 12/05/2018
ms.keywords: ConfigureBYOTSysTxn, ConfigureBYOTSysTxn method [COM+], ConfigureBYOTSysTxn method [COM+],IServiceSysTxnConfig interface, IServiceSysTxnConfig interface [COM+],ConfigureBYOTSysTxn method, IServiceSysTxnConfig.ConfigureBYOTSysTxn, IServiceSysTxnConfig::ConfigureBYOTSysTxn, comsvcs/IServiceSysTxnConfig::ConfigureBYOTSysTxn, cos.iservicesystxnconfig_configurebyotsystxn
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
 - IServiceSysTxnConfig::ConfigureBYOTSysTxn
 - comsvcs/IServiceSysTxnConfig::ConfigureBYOTSysTxn
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
 - IServiceSysTxnConfig.ConfigureBYOTSysTxn
---

# IServiceSysTxnConfig::ConfigureBYOTSysTxn


## -description

Enables you to run the enclosed code in the scope of an existing transaction that you specify with a transaction proxy.

## -parameters

### -param pTxProxy [in]

The <a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionproxy">ITransactionProxy</a> interface of the existing transaction in which you will run the enclosed code.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicesystxnconfig">IServiceSysTxnConfig</a>