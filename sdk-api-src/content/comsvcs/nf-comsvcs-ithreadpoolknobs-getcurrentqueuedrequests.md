---
UID: NF:comsvcs.IThreadPoolKnobs.GetCurrentQueuedRequests
title: IThreadPoolKnobs::GetCurrentQueuedRequests (comsvcs.h)
author: windows-sdk-content
description: Retrieves the number of asynchronous execution requests that are currently queued.
old-location: cos\ithreadpoolknobs_getcurrentqueuedrequests.htm
tech.root: cossdk
ms.assetid: 2ff8ffce-2e53-4e33-bf1d-7d46c5ae12bb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCurrentQueuedRequests, GetCurrentQueuedRequests method [COM+], GetCurrentQueuedRequests method [COM+],IThreadPoolKnobs interface, IThreadPoolKnobs interface [COM+],GetCurrentQueuedRequests method, IThreadPoolKnobs.GetCurrentQueuedRequests, IThreadPoolKnobs::GetCurrentQueuedRequests, _cos_IThreadPoolKnobs_GetCurrentQueuedRequests, comsvcs/IThreadPoolKnobs::GetCurrentQueuedRequests, cos.ithreadpoolknobs_getcurrentqueuedrequests
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
 - IThreadPoolKnobs.GetCurrentQueuedRequests
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IThreadPoolKnobs::GetCurrentQueuedRequests


## -description


Retrieves the number of asynchronous execution requests that are currently queued.


## -parameters




### -param plcCurrentQueuedRequests [out]

The number of asynchronous execution requests currently queued.



## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/3d36e4ec-f4d4-407b-b671-4134886b7a2c">IThreadPoolKnobs</a>
 

 

