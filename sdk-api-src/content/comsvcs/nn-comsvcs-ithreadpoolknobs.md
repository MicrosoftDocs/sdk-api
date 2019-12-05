---
UID: NN:comsvcs.IThreadPoolKnobs
title: IThreadPoolKnobs (comsvcs.h)
description: Used to control the behavior of thread pools.
old-location: cos\ithreadpoolknobs.htm
tech.root: cossdk
ms.assetid: 3d36e4ec-f4d4-407b-b671-4134886b7a2c
ms.date: 12/05/2018
ms.keywords: IThreadPoolKnobs, IThreadPoolKnobs interface [COM+], IThreadPoolKnobs interface [COM+],described, _cos_IThreadPoolKnobs, comsvcs/IThreadPoolKnobs, cos.ithreadpoolknobs
ms.topic: interface
f1_keywords:
- comsvcs/IThreadPoolKnobs
dev_langs:
- c++
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
- IThreadPoolKnobs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IThreadPoolKnobs interface


## -description


Used to control the behavior of thread pools.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IThreadPoolKnobs</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IThreadPoolKnobs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IThreadPoolKnobs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ithreadpoolknobs-getcurrentqueuedrequests">GetCurrentQueuedRequests</a>
</td>
<td align="left" width="63%">
Retrieves the number of asynchronous execution requests that are currently queued.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ithreadpoolknobs-getcurrentthreads">GetCurrentThreads</a>
</td>
<td align="left" width="63%">
Retrieves the number of threads currently in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ithreadpoolknobs-getdeletedelay">GetDeleteDelay</a>
</td>
<td align="left" width="63%">
Retrieves the number of milliseconds a pooled thread can idle before being destroyed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ithreadpoolknobs-getmaxqueuedrequests">GetMaxQueuedRequests</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of asynchronous execution requests that can be simultaneously queued.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ithreadpoolknobs-getmaxthreads">GetMaxThreads</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of threads that are allowed in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ithreadpoolknobs-setdeletedelay">SetDeleteDelay</a>
</td>
<td align="left" width="63%">
Sets the number of milliseconds a pooled thread can idle before being destroyed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ithreadpoolknobs-setmaxqueuedrequests">SetMaxQueuedRequests</a>
</td>
<td align="left" width="63%">
Sets the maximum number of asynchronous execution requests that can be simultaneously queued.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ithreadpoolknobs-setmaxthreads">SetMaxThreads</a>
</td>
<td align="left" width="63%">
Sets the maximum number of threads to be allowed in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ithreadpoolknobs-setminthreads">SetMinThreads</a>
</td>
<td align="left" width="63%">
Sets the minimum number of threads to be maintained in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ithreadpoolknobs-setqueuedepth">SetQueueDepth</a>
</td>
<td align="left" width="63%">
Sets the threshold number of execution requests above which a new thread is added to the pool.

</td>
</tr>
</table> 

