---
UID: NF:comsvcs.IThreadPoolKnobs.SetMaxThreads
title: IThreadPoolKnobs::SetMaxThreads (comsvcs.h)
description: Sets the maximum number of threads to be allowed in the pool.
helpviewer_keywords: ["IThreadPoolKnobs interface [COM+]","SetMaxThreads method","IThreadPoolKnobs.SetMaxThreads","IThreadPoolKnobs::SetMaxThreads","SetMaxThreads","SetMaxThreads method [COM+]","SetMaxThreads method [COM+]","IThreadPoolKnobs interface","_cos_IThreadPoolKnobs_SetMaxThreads","comsvcs/IThreadPoolKnobs::SetMaxThreads","cos.ithreadpoolknobs_setmaxthreads"]
old-location: cos\ithreadpoolknobs_setmaxthreads.htm
tech.root: cos
ms.assetid: abca2ec3-4dcd-4770-a500-1d46b87b4cda
ms.date: 12/05/2018
ms.keywords: IThreadPoolKnobs interface [COM+],SetMaxThreads method, IThreadPoolKnobs.SetMaxThreads, IThreadPoolKnobs::SetMaxThreads, SetMaxThreads, SetMaxThreads method [COM+], SetMaxThreads method [COM+],IThreadPoolKnobs interface, _cos_IThreadPoolKnobs_SetMaxThreads, comsvcs/IThreadPoolKnobs::SetMaxThreads, cos.ithreadpoolknobs_setmaxthreads
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
 - IThreadPoolKnobs::SetMaxThreads
 - comsvcs/IThreadPoolKnobs::SetMaxThreads
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
 - IThreadPoolKnobs.SetMaxThreads
---

# IThreadPoolKnobs::SetMaxThreads


## -description

Sets the maximum number of threads to be allowed in the pool.

## -parameters

### -param lcMaxThreads [in]

The maximum number of threads allowed in the pool. A zero value indicates that the pool can grow without limit.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ithreadpoolknobs">IThreadPoolKnobs</a>