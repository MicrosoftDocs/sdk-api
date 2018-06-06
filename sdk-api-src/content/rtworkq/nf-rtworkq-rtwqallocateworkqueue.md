---
UID: NF:rtworkq.RtwqAllocateWorkQueue
title: RtwqAllocateWorkQueue function
author: windows-sdk-content
description: Creates a new work queue.
old-location: base\rtwqallocateworkqueue.htm
old-project: ProcThread
ms.assetid: B8FF907A-1448-43A4-B249-9D3D859D8F95
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: RTWQ_MULTITHREADED_WORKQUEUE, RTWQ_STANDARD_WORKQUEUE, RTWQ_WINDOW_WORKQUEUE, RtwqAllocateWorkQueue, RtwqAllocateWorkQueue function, base.rtwqallocateworkqueue, rtworkq/RtwqAllocateWorkQueue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: RTWQ_WORKQUEUE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqAllocateWorkQueue
product: Windows
targetos: Windows
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RtwqAllocateWorkQueue function


## -description



          Creates a new work queue.


## -parameters




### -param WorkQueueType [in]

A member of the <a href="https://msdn.microsoft.com/4aab85f3-855e-4fbf-9d25-209214bdd73b">RTWQ_WORKQUEUE_TYPE</a> enumeration, specifying the type of work queue to create.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTWQ_MULTITHREADED_WORKQUEUE"></a><a id="rtwq_multithreaded_workqueue"></a><dl>
<dt><b>RTWQ_MULTITHREADED_WORKQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Create a multithreaded work queue. Generally, applications should not create private multithreaded queues. Use the platform multithreaded queues instead. 

</td>
</tr>
<tr>
<td width="40%"><a id="RTWQ_STANDARD_WORKQUEUE"></a><a id="rtwq_standard_workqueue"></a><dl>
<dt><b>RTWQ_STANDARD_WORKQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Create a work queue without a message loop. Using this flag is equivalent to calling <b>RtwqAllocateWorkQueue</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="RTWQ_WINDOW_WORKQUEUE"></a><a id="rtwq_window_workqueue"></a><dl>
<dt><b>RTWQ_WINDOW_WORKQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Create a work queue with a message loop. The thread that dispatches the work items for this queue will also call <a href="https://msdn.microsoft.com/b9f5baa4-8166-4d6e-b416-df023aed9bad">PeekMessage</a> and <a href="https://msdn.microsoft.com/6d5e2d1d-dcd2-48ce-a8ba-99bd5dbdfb21">DispatchMessage</a>. Use this option if your callback performs any actions that require a message loop.

</td>
</tr>
</table>
 


### -param workQueueId [out]

Receives an identifier for the work queue that was created.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



