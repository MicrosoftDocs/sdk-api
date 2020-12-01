---
UID: NF:comsvcs.IServicePoolConfig.put_MaxPoolSize
title: IServicePoolConfig::put_MaxPoolSize (comsvcs.h)
description: Sets the maximum number of objects in the pool.
helpviewer_keywords: ["IServicePoolConfig interface [COM+]","put_MaxPoolSize method","IServicePoolConfig.put_MaxPoolSize","IServicePoolConfig::put_MaxPoolSize","comsvcs/IServicePoolConfig::put_MaxPoolSize","cos.iservicepoolconfig_put_maxpoolsize","put_MaxPoolSize","put_MaxPoolSize method [COM+]","put_MaxPoolSize method [COM+]","IServicePoolConfig interface"]
old-location: cos\iservicepoolconfig_put_maxpoolsize.htm
tech.root: cos
ms.assetid: 618d4969-c29e-4944-8954-a982a90f3c15
ms.date: 12/05/2018
ms.keywords: IServicePoolConfig interface [COM+],put_MaxPoolSize method, IServicePoolConfig.put_MaxPoolSize, IServicePoolConfig::put_MaxPoolSize, comsvcs/IServicePoolConfig::put_MaxPoolSize, cos.iservicepoolconfig_put_maxpoolsize, put_MaxPoolSize, put_MaxPoolSize method [COM+], put_MaxPoolSize method [COM+],IServicePoolConfig interface
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
 - IServicePoolConfig::put_MaxPoolSize
 - comsvcs/IServicePoolConfig::put_MaxPoolSize
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
 - IServicePoolConfig.put_MaxPoolSize
---

# IServicePoolConfig::put_MaxPoolSize


## -description

Sets the maximum number of objects in the pool.

## -parameters

### -param dwMaxPool [in]

The maximum number of objects.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepoolconfig">IServicePoolConfig</a>