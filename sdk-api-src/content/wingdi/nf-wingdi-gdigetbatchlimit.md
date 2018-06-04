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

# GdiGetBatchLimit function


## -description


The <b>GdiGetBatchLimit</b> function returns the maximum number of function calls that can be accumulated in the calling thread's current batch. The system flushes the current batch whenever this limit is exceeded.


## -parameters






## -returns



If the function succeeds, the return value is the batch limit.

If the function fails, the return value is zero.




## -remarks



The batch limit is set by using the <a href="https://msdn.microsoft.com/53bf0dfe-e93c-401d-ac5d-6717bad2625e">GdiSetBatchLimit</a> function. Setting the limit to 1 effectively disables batching.

Only GDI drawing functions that return Boolean values can be batched; calls to any other GDI functions immediately flush the current batch. Exceeding the batch limit or calling the <a href="https://msdn.microsoft.com/6d2f398d-7a30-4b14-81de-23ab10e1749c">GdiFlush</a> function also flushes the current batch.

When the system batches a function call, the function returns <b>TRUE</b>. The actual return value for the function is reported only if <a href="https://msdn.microsoft.com/6d2f398d-7a30-4b14-81de-23ab10e1749c">GdiFlush</a> is used to flush the batch.

<div class="alert"><b>Note</b>  The batch limit is maintained for each thread separately. In order to completely disable batching, call <a href="https://msdn.microsoft.com/53bf0dfe-e93c-401d-ac5d-6717bad2625e">GdiSetBatchLimit</a> (1) during the initialization of each thread.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6d2f398d-7a30-4b14-81de-23ab10e1749c">
        GdiFlush
      </a>



<a href="https://msdn.microsoft.com/53bf0dfe-e93c-401d-ac5d-6717bad2625e">
        GdiSetBatchLimit
      </a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>
 

 

