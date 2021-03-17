---
UID: NF:comsvcs.IServiceThreadPoolConfig.SelectThreadPool
title: IServiceThreadPoolConfig::SelectThreadPool (comsvcs.h)
description: Selects the thread pool in which the work submitted through the activity is to run.
helpviewer_keywords: ["IServiceThreadPoolConfig interface [COM+]","SelectThreadPool method","IServiceThreadPoolConfig.SelectThreadPool","IServiceThreadPoolConfig::SelectThreadPool","SelectThreadPool","SelectThreadPool method [COM+]","SelectThreadPool method [COM+]","IServiceThreadPoolConfig interface","_cos_IServiceThreadPoolConfig_SelectThreadPool","comsvcs/IServiceThreadPoolConfig::SelectThreadPool","cos.iservicethreadpoolconfig_selectthreadpool"]
old-location: cos\iservicethreadpoolconfig_selectthreadpool.htm
tech.root: cos
ms.assetid: eba8b4fc-aee7-4ba5-8e0e-b74ce9d25a86
ms.date: 12/05/2018
ms.keywords: IServiceThreadPoolConfig interface [COM+],SelectThreadPool method, IServiceThreadPoolConfig.SelectThreadPool, IServiceThreadPoolConfig::SelectThreadPool, SelectThreadPool, SelectThreadPool method [COM+], SelectThreadPool method [COM+],IServiceThreadPoolConfig interface, _cos_IServiceThreadPoolConfig_SelectThreadPool, comsvcs/IServiceThreadPoolConfig::SelectThreadPool, cos.iservicethreadpoolconfig_selectthreadpool
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
 - IServiceThreadPoolConfig::SelectThreadPool
 - comsvcs/IServiceThreadPoolConfig::SelectThreadPool
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
 - IServiceThreadPoolConfig.SelectThreadPool
---

# IServiceThreadPoolConfig::SelectThreadPool


## -description

Selects the thread pool in which the work submitted through the activity is to run.

## -parameters

### -param threadPool [in]

A value from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_threadpool">CSC_ThreadPool</a> enumeration.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicethreadpoolconfig">IServiceThreadPoolConfig</a>