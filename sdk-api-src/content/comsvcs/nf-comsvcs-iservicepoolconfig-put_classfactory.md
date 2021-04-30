---
UID: NF:comsvcs.IServicePoolConfig.put_ClassFactory
title: IServicePoolConfig::put_ClassFactory (comsvcs.h)
description: Sets a class factory for the pooled objects.
helpviewer_keywords: ["IServicePoolConfig interface [COM+]","put_ClassFactory method","IServicePoolConfig.put_ClassFactory","IServicePoolConfig::put_ClassFactory","comsvcs/IServicePoolConfig::put_ClassFactory","cos.iservicepoolconfig_put_classfactory","put_ClassFactory","put_ClassFactory method [COM+]","put_ClassFactory method [COM+]","IServicePoolConfig interface"]
old-location: cos\iservicepoolconfig_put_classfactory.htm
tech.root: cos
ms.assetid: 329c67f0-3c02-4cea-bee6-b5c8aaa9471b
ms.date: 12/05/2018
ms.keywords: IServicePoolConfig interface [COM+],put_ClassFactory method, IServicePoolConfig.put_ClassFactory, IServicePoolConfig::put_ClassFactory, comsvcs/IServicePoolConfig::put_ClassFactory, cos.iservicepoolconfig_put_classfactory, put_ClassFactory, put_ClassFactory method [COM+], put_ClassFactory method [COM+],IServicePoolConfig interface
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
 - IServicePoolConfig::put_ClassFactory
 - comsvcs/IServicePoolConfig::put_ClassFactory
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
 - IServicePoolConfig.put_ClassFactory
---

# IServicePoolConfig::put_ClassFactory


## -description

Sets a class factory for the pooled objects.

## -parameters

### -param pFactory [in]

An <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> interface pointer.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepoolconfig">IServicePoolConfig</a>