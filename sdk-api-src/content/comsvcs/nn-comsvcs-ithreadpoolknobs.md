---
UID: NN:comsvcs.IThreadPoolKnobs
title: IThreadPoolKnobs
author: windows-sdk-content
description: Used to control the behavior of thread pools.
old-location: cos\ithreadpoolknobs.htm
old-project: cossdk
ms.assetid: 3d36e4ec-f4d4-407b-b671-4134886b7a2c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IThreadPoolKnobs, IThreadPoolKnobs interface [COM+], IThreadPoolKnobs interface [COM+],described, _cos_IThreadPoolKnobs, comsvcs/IThreadPoolKnobs, cos.ithreadpoolknobs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IThreadPoolKnobs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IThreadPoolKnobs interface


## -description


Used to control the behavior of thread pools.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IThreadPoolKnobs</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IThreadPoolKnobs</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2ff8ffce-2e53-4e33-bf1d-7d46c5ae12bb">GetCurrentQueuedRequests</a>
</td>
<td align="left" width="63%">
Retrieves the number of asynchronous execution requests that are currently queued.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/138f6c25-5a64-469d-b3fd-d399d43f5084">GetCurrentThreads</a>
</td>
<td align="left" width="63%">
Retrieves the number of threads currently in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93404c39-b4f8-4247-a437-fd373b0b68fe">GetDeleteDelay</a>
</td>
<td align="left" width="63%">
Retrieves the number of milliseconds a pooled thread can idle before being destroyed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/349e6635-5ba6-4b8e-b321-8ffd87cd762c">GetMaxQueuedRequests</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of asynchronous execution requests that can be simultaneously queued.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf99a8f3-fe48-41f3-9162-8550981520a2">GetMaxThreads</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of threads that are allowed in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd01dc40-fbf6-48f9-bef7-8a935a6adf28">SetDeleteDelay</a>
</td>
<td align="left" width="63%">
Sets the number of milliseconds a pooled thread can idle before being destroyed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63f579a0-853e-484b-bc49-1c0f4c76d889">SetMaxQueuedRequests</a>
</td>
<td align="left" width="63%">
Sets the maximum number of asynchronous execution requests that can be simultaneously queued.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abca2ec3-4dcd-4770-a500-1d46b87b4cda">SetMaxThreads</a>
</td>
<td align="left" width="63%">
Sets the maximum number of threads to be allowed in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17852fb8-7e8e-44bb-99f2-b7b7a5053f49">SetMinThreads</a>
</td>
<td align="left" width="63%">
Sets the minimum number of threads to be maintained in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42c12d8b-d7e6-4dd3-926c-176638433839">SetQueueDepth</a>
</td>
<td align="left" width="63%">
Sets the threshold number of execution requests above which a new thread is added to the pool.

</td>
</tr>
</table> 

