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

# IMFRealTimeClientEx::RegisterThreadsEx


## -description


Notifies the object to register its worker threads with the Multimedia Class Scheduler Service (MMCSS).


## -parameters




### -param pdwTaskIndex [in, out]

The MMCSS task identifier. If the value is zero on input,  the object should create a new MCCSS task group. See Remarks.


### -param wszClassName [in]

The name of the MMCSS task.


### -param lBasePriority [in]

The base priority of the thread.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the object does not create worker threads, the method should simply return S_OK and take no further action. 

Otherwise, if the value of <code>*pdwTaskIndex</code> is zero on input, the object should perform the following steps:

<ol>
<li>A single worker thread calls <a href="https://msdn.microsoft.com/881d3f97-e68e-40cb-b799-76784185dd37">AvSetMmThreadCharacteristics</a> to create a new MMCSS task identifier. Store this value.</li>
<li>Any additional worker threads call <a href="https://msdn.microsoft.com/881d3f97-e68e-40cb-b799-76784185dd37">AvSetMmThreadCharacteristics</a> using the new task identifier.</li>
<li>Return the new task identifier to the caller, by setting <code>*pdwTaskIndex</code> equal to the task identifier.</li>
</ol>
If the value of <code>*pdwTaskIndex</code> is nonzero on input, the parameter contains an existing MMCSS task identifer. In that case, all worker threads of the object should register themselves for that task by calling <a href="https://msdn.microsoft.com/881d3f97-e68e-40cb-b799-76784185dd37">AvSetMmThreadCharacteristics</a>.




## -see-also




<a href="https://msdn.microsoft.com/EC5CDD23-B862-4DAE-AC01-4926C4FAD89A">IMFRealTimeClientEx</a>



<a href="https://msdn.microsoft.com/9E2A1D94-BF82-488E-8297-D524683ABE17">Work Queue and Threading Improvements</a>
 

 

