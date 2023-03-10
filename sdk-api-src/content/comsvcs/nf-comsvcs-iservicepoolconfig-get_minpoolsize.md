---
UID: NF:comsvcs.IServicePoolConfig.get_MinPoolSize
title: IServicePoolConfig::get_MinPoolSize (comsvcs.h)
description: Retrieves the minimum number of objects in the pool.
helpviewer_keywords: ["IServicePoolConfig interface [COM+]","get_MinPoolSize method","IServicePoolConfig.get_MinPoolSize","IServicePoolConfig::get_MinPoolSize","comsvcs/IServicePoolConfig::get_MinPoolSize","cos.iservicepoolconfig_get_minpoolsize","get_MinPoolSize","get_MinPoolSize method [COM+]","get_MinPoolSize method [COM+]","IServicePoolConfig interface"]
old-location: cos\iservicepoolconfig_get_minpoolsize.htm
tech.root: cos
ms.assetid: 267e2785-dbff-4b44-8bd5-e7e1e8f69478
ms.date: 12/05/2018
ms.keywords: IServicePoolConfig interface [COM+],get_MinPoolSize method, IServicePoolConfig.get_MinPoolSize, IServicePoolConfig::get_MinPoolSize, comsvcs/IServicePoolConfig::get_MinPoolSize, cos.iservicepoolconfig_get_minpoolsize, get_MinPoolSize, get_MinPoolSize method [COM+], get_MinPoolSize method [COM+],IServicePoolConfig interface
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
 - IServicePoolConfig::get_MinPoolSize
 - comsvcs/IServicePoolConfig::get_MinPoolSize
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
 - IServicePoolConfig.get_MinPoolSize
---

# IServicePoolConfig::get_MinPoolSize


## -description

Retrieves the minimum number of objects in the pool.

## -parameters

### -param pdwMinPool [in]

The minimum number of objects.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepoolconfig">IServicePoolConfig</a>