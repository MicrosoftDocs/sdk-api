---
UID: NF:comsvcs.IThreadPoolKnobs.GetMaxQueuedRequests
title: IThreadPoolKnobs::GetMaxQueuedRequests (comsvcs.h)
description: Retrieves the maximum number of asynchronous execution requests that can be simultaneously queued.
helpviewer_keywords: ["GetMaxQueuedRequests","GetMaxQueuedRequests method [COM+]","GetMaxQueuedRequests method [COM+]","IThreadPoolKnobs interface","IThreadPoolKnobs interface [COM+]","GetMaxQueuedRequests method","IThreadPoolKnobs.GetMaxQueuedRequests","IThreadPoolKnobs::GetMaxQueuedRequests","_cos_IThreadPoolKnobs_GetMaxQueuedRequests","comsvcs/IThreadPoolKnobs::GetMaxQueuedRequests","cos.ithreadpoolknobs_getmaxqueuedrequests"]
old-location: cos\ithreadpoolknobs_getmaxqueuedrequests.htm
tech.root: cos
ms.assetid: 349e6635-5ba6-4b8e-b321-8ffd87cd762c
ms.date: 12/05/2018
ms.keywords: GetMaxQueuedRequests, GetMaxQueuedRequests method [COM+], GetMaxQueuedRequests method [COM+],IThreadPoolKnobs interface, IThreadPoolKnobs interface [COM+],GetMaxQueuedRequests method, IThreadPoolKnobs.GetMaxQueuedRequests, IThreadPoolKnobs::GetMaxQueuedRequests, _cos_IThreadPoolKnobs_GetMaxQueuedRequests, comsvcs/IThreadPoolKnobs::GetMaxQueuedRequests, cos.ithreadpoolknobs_getmaxqueuedrequests
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
 - IThreadPoolKnobs::GetMaxQueuedRequests
 - comsvcs/IThreadPoolKnobs::GetMaxQueuedRequests
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
 - IThreadPoolKnobs.GetMaxQueuedRequests
---

# IThreadPoolKnobs::GetMaxQueuedRequests


## -description

Retrieves the maximum number of asynchronous execution requests that can be simultaneously queued.

## -parameters

### -param plcMaxQueuedRequests [out]

The maximum number of asynchronous execution requests that can be simultaneously queued. A zero value indicates that the queue can grow without limit.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ithreadpoolknobs">IThreadPoolKnobs</a>