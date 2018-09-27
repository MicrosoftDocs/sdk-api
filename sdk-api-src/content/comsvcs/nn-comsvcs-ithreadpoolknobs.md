---
UID: NN:comsvcs.IThreadPoolKnobs
title: IThreadPoolKnobs
author: windows-sdk-content
description: Used to control the behavior of thread pools.
old-location: cos\ithreadpoolknobs.htm
tech.root: cossdk
ms.assetid: 3d36e4ec-f4d4-407b-b671-4134886b7a2c
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IThreadPoolKnobs, IThreadPoolKnobs interface [COM+], IThreadPoolKnobs interface [COM+],described, _cos_IThreadPoolKnobs, comsvcs/IThreadPoolKnobs, cos.ithreadpoolknobs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/ms684244(v=VS.85).aspx">GetDeleteDelay</a>
</td>
<td align="left" width="63%">
Retrieves the number of milliseconds a pooled thread can idle before being destroyed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679804(v=VS.85).aspx">GetMaxQueuedRequests</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of asynchronous execution requests that can be simultaneously queued.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686532(v=VS.85).aspx">GetMaxThreads</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of threads that are allowed in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687006(v=VS.85).aspx">SetDeleteDelay</a>
</td>
<td align="left" width="63%">
Sets the number of milliseconds a pooled thread can idle before being destroyed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681796(v=VS.85).aspx">SetMaxQueuedRequests</a>
</td>
<td align="left" width="63%">
Sets the maximum number of asynchronous execution requests that can be simultaneously queued.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685191(v=VS.85).aspx">SetMaxThreads</a>
</td>
<td align="left" width="63%">
Sets the maximum number of threads to be allowed in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679192(v=VS.85).aspx">SetMinThreads</a>
</td>
<td align="left" width="63%">
Sets the minimum number of threads to be maintained in the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms680625(v=VS.85).aspx">SetQueueDepth</a>
</td>
<td align="left" width="63%">
Sets the threshold number of execution requests above which a new thread is added to the pool.

</td>
</tr>
</table> 

