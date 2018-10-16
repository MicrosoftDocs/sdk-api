---
UID: NF:mfapi.MFLockSharedWorkQueue
title: MFLockSharedWorkQueue function
author: windows-sdk-content
description: Obtains and locks a shared work queue.
old-location: mf\mflocksharedworkqueue.htm
tech.root: medfound
ms.assetid: 1E3AA1EE-83A4-42DE-961E-D93A34CE80CF
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: MFLockSharedWorkQueue, MFLockSharedWorkQueue function [Media Foundation], mf.mflocksharedworkqueue, mfapi/MFLockSharedWorkQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFLockSharedWorkQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFLockSharedWorkQueue function


## -description


Obtains and locks a shared work queue.


## -parameters




### -param wszClass [in]

The name of the MMCSS task. 




### -param BasePriority [in]

The base priority of the work-queue threads. 

If the regular-priority queue is being used (<i>wszClass</i>=""), then the value 0 must be passed in.


### -param pdwTaskId [in, out]

The MMCSS task identifier. On input, specify an existing MCCSS task group ID , or use the value zero to create a new task group. If the regular priority queue is being used (<i>wszClass</i>=""), then <b>NULL</b> must be passed in. On output, receives the actual task group ID.




### -param pID [out]

Receives an identifier for the new work queue. Use this identifier when queuing work items.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A <i>multithreaded work queue</i> uses a thread pool to dispatch work items. Whenever a thread becomes available, it dequeues the next work item from the queue. Work items are dequeued in first-in-first-out order, but work items are not serialized. In other words, the work queue does not wait for a work item to complete before it starts the next work item. 

Within a single process, the Microsoft Media Foundation platform creates up to one multithreaded queue for each Multimedia Class Scheduler Service (MMCSS) task. The <b>MFLockSharedWorkQueue</b> function checks whether a matching work queue already exists. If not, the function creates a new work queue and registers the work queue with MMCSS. The function returns the MMCSS task identifier (<i>pdwTaskId</i>) and the work queue identifier (<i>pID</i>). To queue a work item, pass the work queue identifier to any of the following functions: 

<ul>
<li>
<a href="https://msdn.microsoft.com/b0233589-2a55-4803-9dcb-85d757734dee">MFPutWorkItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C49818B3-83FF-40CE-B68A-F60F3277F7B8">MFPutWorkItem2</a>
</li>
<li>
<a href="https://msdn.microsoft.com/67b4f7c6-0d49-4ed0-9bc3-e583451884af">MFPutWorkItemEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A29DC852-AF0F-4269-97FB-DA1F725E7C09">MFPutWorkItemEx2</a>
</li>
</ul>
The <b>MFLockSharedWorkQueue</b> function also locks the queue. Before the process exits, call <a href="https://msdn.microsoft.com/bbc22fa7-b4d7-47b2-b065-099fbb2ed092">MFUnlockWorkQueue</a> to unlock the work queue.

If the regular priority queue is being used (<i>wszClass</i>=""), then NULL must be passed in to <i>pdwTaskId</i> and the value 0 must be passed into <i>BasePriority</i>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/9E2A1D94-BF82-488E-8297-D524683ABE17">Work Queue and Threading Improvements</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

