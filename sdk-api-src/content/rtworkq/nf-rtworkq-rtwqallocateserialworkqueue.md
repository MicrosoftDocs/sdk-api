---
UID: NF:rtworkq.RtwqAllocateSerialWorkQueue
title: RtwqAllocateSerialWorkQueue function (rtworkq.h)
description: Creates a virtual work queue on top of another work queue that is guaranteed to serialize work items. The serial work queue wraps an existing multithreaded work queue. The serial work queue enforces a first-in, first-out (FIFO) execution order.
helpviewer_keywords: ["RtwqAllocateSerialWorkQueue","RtwqAllocateSerialWorkQueue function","base.rtwqallocateserialworkqueue","rtworkq/RtwqAllocateSerialWorkQueue"]
old-location: base\rtwqallocateserialworkqueue.htm
tech.root: backup
ms.assetid: e2021bf3-40d8-4697-b82f-eebee2140a6e
ms.date: 12/05/2018
ms.keywords: RtwqAllocateSerialWorkQueue, RtwqAllocateSerialWorkQueue function, base.rtwqallocateserialworkqueue, rtworkq/RtwqAllocateSerialWorkQueue
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtwqAllocateSerialWorkQueue
 - rtworkq/RtwqAllocateSerialWorkQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqAllocateSerialWorkQueue
---

# RtwqAllocateSerialWorkQueue function


## -description

Creates a virtual  work queue on top of another work queue that is guaranteed to serialize work items. The serial work queue wraps an existing multithreaded work queue. The serial work queue enforces a first-in, first-out (FIFO) execution order.

## -parameters

### -param workQueueIdIn [in]

The identifier of an existing work queue. This must be either a multithreaded queue or another serial work queue. Any of the following can be used:

<ul>
<li>The default work queue  (<b>RTWQ_STANDARD_WORKQUEUE</b>).  See <a href="/windows/desktop/api/rtworkq/ne-rtworkq-rtwq_workqueue_type">RTWQ_WORKQUEUE_TYPE</a>.</li>
<li>The platform multithreaded queue (<b>RTWQ_MULTITHREADED_WORKQUEUE</b>). See <a href="/windows/desktop/api/rtworkq/ne-rtworkq-rtwq_workqueue_type">RTWQ_WORKQUEUE_TYPE</a>.</li>
<li>A multithreaded queue returned by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqlocksharedworkqueue">RtwqLockSharedWorkQueue</a>  function.</li>
<li>A serial queue created by the <b>RtwqAllocateSerialWorkQueue</b> function.</li>
</ul>

### -param workQueueIdOut [out]

Receives an identifier for the new serial work queue. Use this identifier when queuing work items.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The application exceeded the maximum number of work queues.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RTWQ_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The application did not call <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqstartup">RtwqStartup</a>, or the application has already called <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqshutdown">RtwqShutdown</a>.
              

</td>
</tr>
</table>

## -remarks

When you are done using the work queue, call <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqunlockworkqueue">RtwqUnlockWorkQueue</a>.

Multithreaded queues use a thread pool, which  can reduce the total number of threads in the pipeline. However, they do not serialize work items. A serial work queue enables the application to get the benefits of the thread pool, without needing to perform manual serialization of its own work items.

## -see-also

<a href="/windows/desktop/api/rtworkq/ne-rtworkq-rtwq_workqueue_type">RTWQ_WORKQUEUE_TYPE</a>