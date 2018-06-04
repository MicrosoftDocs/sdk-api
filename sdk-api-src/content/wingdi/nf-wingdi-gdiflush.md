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

# GdiFlush function


## -description


The <b>GdiFlush</b> function flushes the calling thread's current batch.


## -parameters






## -returns



If all functions in the current batch succeed, the return value is nonzero.

If not all functions in the current batch succeed, the return value is zero, indicating that at least one function returned an error.




## -remarks



Batching enhances drawing performance by minimizing the amount of time needed to call GDI drawing functions that return Boolean values. The system accumulates the parameters for calls to these functions in the current batch and then calls the functions when the batch is flushed by any of the following means:

<ul>
<li>Calling the <b>GdiFlush</b> function.</li>
<li>Reaching or exceeding the batch limit set by the <a href="https://msdn.microsoft.com/53bf0dfe-e93c-401d-ac5d-6717bad2625e">GdiSetBatchLimit</a> function.</li>
<li>Filling the batching buffers.</li>
<li>Calling any GDI function that does not return a Boolean value.</li>
</ul>
The return value for <b>GdiFlush</b> applies only to the functions in the batch at the time <b>GdiFlush</b> is called. Errors that occur when the batch is flushed by any other means are never reported.

The <a href="https://msdn.microsoft.com/aafe7635-1a71-42a9-90b7-11179e245af4">GdiGetBatchLimit</a> function returns the batch limit.

<div class="alert"><b>Note</b>  The batch limit is maintained for each thread separately. In order to completely disable batching, call <a href="https://msdn.microsoft.com/53bf0dfe-e93c-401d-ac5d-6717bad2625e">GdiSetBatchLimit</a> (1) during the initialization of each thread.</div>
<div> </div>
An application should call <b>GdiFlush</b> before a thread goes away if there is a possibility that there are pending function calls in the graphics batch queue. The system does not execute such batched functions when a thread goes away.

A multithreaded application that serializes access to GDI objects with a mutex must ensure flushing the GDI batch queue by calling <b>GdiFlush</b> as each thread releases ownership of the GDI object. This prevents collisions of the GDI objects (device contexts, metafiles, and so on).




## -see-also




<a href="https://msdn.microsoft.com/aafe7635-1a71-42a9-90b7-11179e245af4">
        GdiGetBatchLimit
      </a>



<a href="https://msdn.microsoft.com/53bf0dfe-e93c-401d-ac5d-6717bad2625e">
        GdiSetBatchLimit
      </a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>
 

 

