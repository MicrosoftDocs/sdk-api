---
UID: NF:comsvcs.IServicePoolConfig.put_MinPoolSize
title: IServicePoolConfig::put_MinPoolSize (comsvcs.h)
description: Sets the minimum number of objects in the pool.
helpviewer_keywords: ["IServicePoolConfig interface [COM+]","put_MinPoolSize method","IServicePoolConfig.put_MinPoolSize","IServicePoolConfig::put_MinPoolSize","comsvcs/IServicePoolConfig::put_MinPoolSize","cos.iservicepoolconfig_put_minpoolsize","put_MinPoolSize","put_MinPoolSize method [COM+]","put_MinPoolSize method [COM+]","IServicePoolConfig interface"]
old-location: cos\iservicepoolconfig_put_minpoolsize.htm
tech.root: cos
ms.assetid: 6280b4ed-704e-464e-bde2-64c1f2353730
ms.date: 12/05/2018
ms.keywords: IServicePoolConfig interface [COM+],put_MinPoolSize method, IServicePoolConfig.put_MinPoolSize, IServicePoolConfig::put_MinPoolSize, comsvcs/IServicePoolConfig::put_MinPoolSize, cos.iservicepoolconfig_put_minpoolsize, put_MinPoolSize, put_MinPoolSize method [COM+], put_MinPoolSize method [COM+],IServicePoolConfig interface
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
 - IServicePoolConfig::put_MinPoolSize
 - comsvcs/IServicePoolConfig::put_MinPoolSize
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
 - IServicePoolConfig.put_MinPoolSize
---

# IServicePoolConfig::put_MinPoolSize


## -description

Sets the minimum number of objects in the pool.

## -parameters

### -param dwMinPool [in]

The minimum number of objects.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepoolconfig">IServicePoolConfig</a>