---
UID: NF:comsvcs.IThreadPoolKnobs.SetQueueDepth
title: IThreadPoolKnobs::SetQueueDepth (comsvcs.h)
author: windows-sdk-content
description: Sets the threshold number of execution requests above which a new thread is added to the pool.
old-location: cos\ithreadpoolknobs_setqueuedepth.htm
tech.root: cossdk
ms.assetid: 42c12d8b-d7e6-4dd3-926c-176638433839
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IThreadPoolKnobs interface [COM+],SetQueueDepth method, IThreadPoolKnobs.SetQueueDepth, IThreadPoolKnobs::SetQueueDepth, SetQueueDepth, SetQueueDepth method [COM+], SetQueueDepth method [COM+],IThreadPoolKnobs interface, _cos_IThreadPoolKnobs_SetQueueDepth, comsvcs/IThreadPoolKnobs::SetQueueDepth, cos.ithreadpoolknobs_setqueuedepth
ms.topic: method
f1_keywords: ["comsvcs/IThreadPoolKnobs.SetQueueDepth"]
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
 - IThreadPoolKnobs.SetQueueDepth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IThreadPoolKnobs::SetQueueDepth


## -description


Sets the threshold number of execution requests above which a new thread is added to the pool.


## -parameters




### -param lcQueueDepth [in]

The threshold number of execution requests above which a new thread is added to the pool.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-ithreadpoolknobs">IThreadPoolKnobs</a>
 

 

