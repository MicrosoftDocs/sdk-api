---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RtwqAllocateSerialWorkQueue function


## -description


Creates a virtual  work queue on top of another work queue that is guaranteed to serialize work items. The serial work queue wraps an existing multithreaded work queue. The serial work queue enforces a first-in, first-out (FIFO) execution order.


## -parameters




### -param workQueueIdIn [in]


            The identifier of an existing work queue. This must be either a multithreaded queue or another serial work queue. Any of the following can be used:

<ul>
<li>The default work queue  (<b>RTWQ_STANDARD_WORKQUEUE</b>).  See <a href="https://msdn.microsoft.com/4aab85f3-855e-4fbf-9d25-209214bdd73b">RTWQ_WORKQUEUE_TYPE</a>.</li>
<li>The platform multithreaded queue (<b>RTWQ_MULTITHREADED_WORKQUEUE</b>). See <a href="https://msdn.microsoft.com/4aab85f3-855e-4fbf-9d25-209214bdd73b">RTWQ_WORKQUEUE_TYPE</a>.</li>
<li>A multithreaded queue returned by the <a href="https://msdn.microsoft.com/ccebdbd8-fd3e-4e99-b1dd-1ec8e57cbff6">RtwqLockSharedWorkQueue</a>  function.</li>
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

                The application did not call <a href="https://msdn.microsoft.com/101e73ec-34ec-49af-999d-5410f46ff319">RtwqStartup</a>, or the application has already called <a href="https://msdn.microsoft.com/806c4142-b628-4ea0-b5e2-d2b4ead73c04">RtwqShutdown</a>.
              

</td>
</tr>
</table>
 




## -remarks



When you are done using the work queue, call <a href="https://msdn.microsoft.com/a7c4c8e2-ad35-4b39-9174-41e2a605304e">RtwqUnlockWorkQueue</a>.

Multithreaded queues use a thread pool, which  can reduce the total number of threads in the pipeline. However, they do not serialize work items. A serial work queue enables the application to get the benefits of the thread pool, without needing to perform manual serialization of its own work items.




## -see-also




<a href="https://msdn.microsoft.com/4aab85f3-855e-4fbf-9d25-209214bdd73b">RTWQ_WORKQUEUE_TYPE</a>
 

 

