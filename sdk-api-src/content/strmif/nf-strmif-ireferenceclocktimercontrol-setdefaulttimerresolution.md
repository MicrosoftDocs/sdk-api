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

# IReferenceClockTimerControl::SetDefaultTimerResolution


## -description


The <code>SetDefaultTimerResolution</code> method sets the minimum timer resolution.


## -parameters




### -param timerResolution [in]

Minimum timer resolution, in 100-nanosecond units. If the value is zero, the reference clock cancels its previous request.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
</table>
 




## -remarks



The reference clock attempts to set the period of the timer to <i>timerResolution</i>. The actual period of the timer might differ, depending on the hardware. To find the minimum and maximum timer resolution, call the <a href="https://msdn.microsoft.com/7b5a9675-1152-4c9e-bc79-fe9afa5c563c">timeGetDevCaps</a> function. The reference clock sets the timer resolution is set by calling <a href="https://msdn.microsoft.com/7168981c-9af8-4665-88a2-7d96a8f2b273">timeBeginPeriod</a>. If <i>timerResolution</i> is 0, the method cancels the previous timer request by calling <a href="https://msdn.microsoft.com/b06531f9-4fd7-4051-80d4-5a175fdd37e7">timeEndPeriod</a>. (When the reference clock is destroyed, it automatically cancels any previous request.)

If this method is not called, the reference clock sets the timer resolution to 1 millisecond. To get the best power management performance, it is recommended that you call this method with the value zero. This overrides the clock's default setting of 1 millisecond. If any filters in the graph require a higher timer resolution, they can call <a href="https://msdn.microsoft.com/7168981c-9af8-4665-88a2-7d96a8f2b273">timeBeginPeriod</a> individually. Typically only renderers should require a particular timer resolution.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/08638917-88b1-42f0-8324-ae6fb9afe5bd">IReferenceClockTimerControl Interface</a>
 

 

