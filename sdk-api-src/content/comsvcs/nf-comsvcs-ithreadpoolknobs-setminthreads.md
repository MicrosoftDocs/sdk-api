---
UID: NF:comsvcs.IThreadPoolKnobs.SetMinThreads
title: IThreadPoolKnobs::SetMinThreads (comsvcs.h)
description: Sets the minimum number of threads to be maintained in the pool.
helpviewer_keywords: ["IThreadPoolKnobs interface [COM+]","SetMinThreads method","IThreadPoolKnobs.SetMinThreads","IThreadPoolKnobs::SetMinThreads","SetMinThreads","SetMinThreads method [COM+]","SetMinThreads method [COM+]","IThreadPoolKnobs interface","_cos_IThreadPoolKnobs_SetMinThreads","comsvcs/IThreadPoolKnobs::SetMinThreads","cos.ithreadpoolknobs_setminthreads"]
old-location: cos\ithreadpoolknobs_setminthreads.htm
tech.root: cos
ms.assetid: 17852fb8-7e8e-44bb-99f2-b7b7a5053f49
ms.date: 12/05/2018
ms.keywords: IThreadPoolKnobs interface [COM+],SetMinThreads method, IThreadPoolKnobs.SetMinThreads, IThreadPoolKnobs::SetMinThreads, SetMinThreads, SetMinThreads method [COM+], SetMinThreads method [COM+],IThreadPoolKnobs interface, _cos_IThreadPoolKnobs_SetMinThreads, comsvcs/IThreadPoolKnobs::SetMinThreads, cos.ithreadpoolknobs_setminthreads
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
 - IThreadPoolKnobs::SetMinThreads
 - comsvcs/IThreadPoolKnobs::SetMinThreads
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
 - IThreadPoolKnobs.SetMinThreads
---

# IThreadPoolKnobs::SetMinThreads


## -description

Sets the minimum number of threads to be maintained in the pool.

## -parameters

### -param lcMinThreads [in]

The minimum number of threads to be maintained in the pool.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ithreadpoolknobs">IThreadPoolKnobs</a>