---
UID: NF:comsvcs.IThreadPoolKnobs.GetCurrentThreads
title: IThreadPoolKnobs::GetCurrentThreads (comsvcs.h)
description: Retrieves the number of threads currently in the pool.
helpviewer_keywords: ["GetCurrentThreads","GetCurrentThreads method [COM+]","GetCurrentThreads method [COM+]","IThreadPoolKnobs interface","IThreadPoolKnobs interface [COM+]","GetCurrentThreads method","IThreadPoolKnobs.GetCurrentThreads","IThreadPoolKnobs::GetCurrentThreads","_cos_IThreadPoolKnobs_GetCurrentThreads","comsvcs/IThreadPoolKnobs::GetCurrentThreads","cos.ithreadpoolknobs_getcurrentthreads"]
old-location: cos\ithreadpoolknobs_getcurrentthreads.htm
tech.root: cos
ms.assetid: 138f6c25-5a64-469d-b3fd-d399d43f5084
ms.date: 12/05/2018
ms.keywords: GetCurrentThreads, GetCurrentThreads method [COM+], GetCurrentThreads method [COM+],IThreadPoolKnobs interface, IThreadPoolKnobs interface [COM+],GetCurrentThreads method, IThreadPoolKnobs.GetCurrentThreads, IThreadPoolKnobs::GetCurrentThreads, _cos_IThreadPoolKnobs_GetCurrentThreads, comsvcs/IThreadPoolKnobs::GetCurrentThreads, cos.ithreadpoolknobs_getcurrentthreads
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
 - IThreadPoolKnobs::GetCurrentThreads
 - comsvcs/IThreadPoolKnobs::GetCurrentThreads
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
 - IThreadPoolKnobs.GetCurrentThreads
---

# IThreadPoolKnobs::GetCurrentThreads


## -description

Retrieves the number of threads currently in the pool.

## -parameters

### -param plcCurrentThreads [out]

The number of threads currently in the pool.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ithreadpoolknobs">IThreadPoolKnobs</a>