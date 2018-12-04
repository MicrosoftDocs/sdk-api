---
UID: NF:comsvcs.IThreadPoolKnobs.SetMaxQueuedRequests
title: IThreadPoolKnobs::SetMaxQueuedRequests
author: windows-sdk-content
description: Sets the maximum number of asynchronous execution requests that can be simultaneously queued.
old-location: cos\ithreadpoolknobs_setmaxqueuedrequests.htm
tech.root: cossdk
ms.assetid: 63f579a0-853e-484b-bc49-1c0f4c76d889
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IThreadPoolKnobs interface [COM+],SetMaxQueuedRequests method, IThreadPoolKnobs.SetMaxQueuedRequests, IThreadPoolKnobs::SetMaxQueuedRequests, SetMaxQueuedRequests, SetMaxQueuedRequests method [COM+], SetMaxQueuedRequests method [COM+],IThreadPoolKnobs interface, _cos_IThreadPoolKnobs_SetMaxQueuedRequests, comsvcs/IThreadPoolKnobs::SetMaxQueuedRequests, cos.ithreadpoolknobs_setmaxqueuedrequests
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IThreadPoolKnobs.SetMaxQueuedRequests
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/3d36e4ec-f4d4-407b-b671-4134886b7a2c">IThreadPoolKnobs</a>
 

 

