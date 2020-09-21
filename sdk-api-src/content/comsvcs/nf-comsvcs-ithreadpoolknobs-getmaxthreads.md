---
UID: NF:comsvcs.IThreadPoolKnobs.GetMaxThreads
title: IThreadPoolKnobs::GetMaxThreads (comsvcs.h)
description: Retrieves the maximum number of threads that are allowed in the pool.
helpviewer_keywords: ["GetMaxThreads","GetMaxThreads method [COM+]","GetMaxThreads method [COM+]","IThreadPoolKnobs interface","IThreadPoolKnobs interface [COM+]","GetMaxThreads method","IThreadPoolKnobs.GetMaxThreads","IThreadPoolKnobs::GetMaxThreads","_cos_IThreadPoolKnobs_GetMaxThreads","comsvcs/IThreadPoolKnobs::GetMaxThreads","cos.ithreadpoolknobs_getmaxthreads"]
old-location: cos\ithreadpoolknobs_getmaxthreads.htm
tech.root: cos
ms.assetid: cf99a8f3-fe48-41f3-9162-8550981520a2
ms.date: 12/05/2018
ms.keywords: GetMaxThreads, GetMaxThreads method [COM+], GetMaxThreads method [COM+],IThreadPoolKnobs interface, IThreadPoolKnobs interface [COM+],GetMaxThreads method, IThreadPoolKnobs.GetMaxThreads, IThreadPoolKnobs::GetMaxThreads, _cos_IThreadPoolKnobs_GetMaxThreads, comsvcs/IThreadPoolKnobs::GetMaxThreads, cos.ithreadpoolknobs_getmaxthreads
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IThreadPoolKnobs::GetMaxThreads
 - comsvcs/IThreadPoolKnobs::GetMaxThreads
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
 - IThreadPoolKnobs.GetMaxThreads
---

# IThreadPoolKnobs::GetMaxThreads


## -description

Retrieves the maximum number of threads that are allowed in the pool.

## -parameters

### -param plcMaxThreads [out]

The maximum number of threads allowed in the pool. A zero value indicates that the pool can grow without limit.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ithreadpoolknobs">IThreadPoolKnobs</a>