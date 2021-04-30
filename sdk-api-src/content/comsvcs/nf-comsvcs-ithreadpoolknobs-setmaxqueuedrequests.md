---
UID: NF:comsvcs.IThreadPoolKnobs.SetMaxQueuedRequests
title: IThreadPoolKnobs::SetMaxQueuedRequests (comsvcs.h)
description: Sets the maximum number of asynchronous execution requests that can be simultaneously queued.
helpviewer_keywords: ["IThreadPoolKnobs interface [COM+]","SetMaxQueuedRequests method","IThreadPoolKnobs.SetMaxQueuedRequests","IThreadPoolKnobs::SetMaxQueuedRequests","SetMaxQueuedRequests","SetMaxQueuedRequests method [COM+]","SetMaxQueuedRequests method [COM+]","IThreadPoolKnobs interface","_cos_IThreadPoolKnobs_SetMaxQueuedRequests","comsvcs/IThreadPoolKnobs::SetMaxQueuedRequests","cos.ithreadpoolknobs_setmaxqueuedrequests"]
old-location: cos\ithreadpoolknobs_setmaxqueuedrequests.htm
tech.root: cos
ms.assetid: 63f579a0-853e-484b-bc49-1c0f4c76d889
ms.date: 12/05/2018
ms.keywords: IThreadPoolKnobs interface [COM+],SetMaxQueuedRequests method, IThreadPoolKnobs.SetMaxQueuedRequests, IThreadPoolKnobs::SetMaxQueuedRequests, SetMaxQueuedRequests, SetMaxQueuedRequests method [COM+], SetMaxQueuedRequests method [COM+],IThreadPoolKnobs interface, _cos_IThreadPoolKnobs_SetMaxQueuedRequests, comsvcs/IThreadPoolKnobs::SetMaxQueuedRequests, cos.ithreadpoolknobs_setmaxqueuedrequests
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
 - IThreadPoolKnobs::SetMaxQueuedRequests
 - comsvcs/IThreadPoolKnobs::SetMaxQueuedRequests
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
 - IThreadPoolKnobs.SetMaxQueuedRequests
---

# IThreadPoolKnobs::SetMaxQueuedRequests


## -description

Sets the maximum number of asynchronous execution requests that can be simultaneously queued.

## -parameters

### -param lcMaxQueuedRequests [in]

The maximum number of asynchronous execution requests that can be simultaneously queued. A zero value indicates that the queue can grow without limit.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ithreadpoolknobs">IThreadPoolKnobs</a>