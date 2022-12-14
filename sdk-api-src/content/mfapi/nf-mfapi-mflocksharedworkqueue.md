---
UID: NF:mfapi.MFLockSharedWorkQueue
title: MFLockSharedWorkQueue function (mfapi.h)
description: Obtains and locks a shared work queue. (MFLockSharedWorkQueue)
helpviewer_keywords: ["MFLockSharedWorkQueue","MFLockSharedWorkQueue function [Media Foundation]","mf.mflocksharedworkqueue","mfapi/MFLockSharedWorkQueue"]
old-location: mf\mflocksharedworkqueue.htm
tech.root: mf
ms.assetid: 1E3AA1EE-83A4-42DE-961E-D93A34CE80CF
ms.date: 12/05/2018
ms.keywords: MFLockSharedWorkQueue, MFLockSharedWorkQueue function [Media Foundation], mf.mflocksharedworkqueue, mfapi/MFLockSharedWorkQueue
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFLockSharedWorkQueue
 - mfapi/MFLockSharedWorkQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFLockSharedWorkQueue
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

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A <i>multithreaded work queue</i> uses a thread pool to dispatch work items. Whenever a thread becomes available, it dequeues the next work item from the queue. Work items are dequeued in first-in-first-out order, but work items are not serialized. In other words, the work queue does not wait for a work item to complete before it starts the next work item. 

Within a single process, the Microsoft Media Foundation platform creates up to one multithreaded queue for each Multimedia Class Scheduler Service (MMCSS) task. The <b>MFLockSharedWorkQueue</b> function checks whether a matching work queue already exists. If not, the function creates a new work queue and registers the work queue with MMCSS. The function returns the MMCSS task identifier (<i>pdwTaskId</i>) and the work queue identifier (<i>pID</i>). To queue a work item, pass the work queue identifier to any of the following functions: 

<ul>
<li>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem">MFPutWorkItem</a>
</li>
<li>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem2">MFPutWorkItem2</a>
</li>
<li>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex">MFPutWorkItemEx</a>
</li>
<li>
<a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex2">MFPutWorkItemEx2</a>
</li>
</ul>
The <b>MFLockSharedWorkQueue</b> function also locks the queue. Before the process exits, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue">MFUnlockWorkQueue</a> to unlock the work queue.

If the regular priority queue is being used (<i>wszClass</i>=""), then NULL must be passed in to <i>pdwTaskId</i> and the value 0 must be passed into <i>BasePriority</i>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
