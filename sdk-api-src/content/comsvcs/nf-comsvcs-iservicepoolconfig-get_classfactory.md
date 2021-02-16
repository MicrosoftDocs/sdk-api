---
UID: NF:comsvcs.IServicePoolConfig.get_ClassFactory
title: IServicePoolConfig::get_ClassFactory (comsvcs.h)
description: Retrieves a class factory for the pooled objects.
helpviewer_keywords: ["IServicePoolConfig interface [COM+]","get_ClassFactory method","IServicePoolConfig.get_ClassFactory","IServicePoolConfig::get_ClassFactory","comsvcs/IServicePoolConfig::get_ClassFactory","cos.iservicepoolconfig_get_classfactory","get_ClassFactory","get_ClassFactory method [COM+]","get_ClassFactory method [COM+]","IServicePoolConfig interface"]
old-location: cos\iservicepoolconfig_get_classfactory.htm
tech.root: cos
ms.assetid: cef9ff6b-53e2-43e1-9be6-7c0d7f89c318
ms.date: 12/05/2018
ms.keywords: IServicePoolConfig interface [COM+],get_ClassFactory method, IServicePoolConfig.get_ClassFactory, IServicePoolConfig::get_ClassFactory, comsvcs/IServicePoolConfig::get_ClassFactory, cos.iservicepoolconfig_get_classfactory, get_ClassFactory, get_ClassFactory method [COM+], get_ClassFactory method [COM+],IServicePoolConfig interface
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
 - IServicePoolConfig::get_ClassFactory
 - comsvcs/IServicePoolConfig::get_ClassFactory
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
 - IServicePoolConfig.get_ClassFactory
---

# IServicePoolConfig::get_ClassFactory


## -description

Retrieves a class factory for the pooled objects.

## -parameters

### -param pFactory [out]

A pointer to the <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> interface pointer.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepoolconfig">IServicePoolConfig</a>