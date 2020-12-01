---
UID: NF:comsvcs.IServicePoolConfig.get_MaxPoolSize
title: IServicePoolConfig::get_MaxPoolSize (comsvcs.h)
description: Retrieves the maximum number of objects in the pool.
helpviewer_keywords: ["IServicePoolConfig interface [COM+]","get_MaxPoolSize method","IServicePoolConfig.get_MaxPoolSize","IServicePoolConfig::get_MaxPoolSize","comsvcs/IServicePoolConfig::get_MaxPoolSize","cos.iservicepoolconfig_get_maxpoolsize","get_MaxPoolSize","get_MaxPoolSize method [COM+]","get_MaxPoolSize method [COM+]","IServicePoolConfig interface"]
old-location: cos\iservicepoolconfig_get_maxpoolsize.htm
tech.root: cos
ms.assetid: b9fb76d4-d153-4968-ad1c-79036b4bb8a4
ms.date: 12/05/2018
ms.keywords: IServicePoolConfig interface [COM+],get_MaxPoolSize method, IServicePoolConfig.get_MaxPoolSize, IServicePoolConfig::get_MaxPoolSize, comsvcs/IServicePoolConfig::get_MaxPoolSize, cos.iservicepoolconfig_get_maxpoolsize, get_MaxPoolSize, get_MaxPoolSize method [COM+], get_MaxPoolSize method [COM+],IServicePoolConfig interface
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
 - IServicePoolConfig::get_MaxPoolSize
 - comsvcs/IServicePoolConfig::get_MaxPoolSize
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
 - IServicePoolConfig.get_MaxPoolSize
---

# IServicePoolConfig::get_MaxPoolSize


## -description

Retrieves the maximum number of objects in the pool.

## -parameters

### -param pdwMaxPool [out]

The maximum number of objects.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepoolconfig">IServicePoolConfig</a>