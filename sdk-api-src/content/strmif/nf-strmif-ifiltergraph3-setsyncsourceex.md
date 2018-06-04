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

# IFilterGraph3::SetSyncSourceEx


## -description



The <code>SetSyncSourceEx</code> method establishes two reference clocks for the filter graph: a primary clock that is used by most of the filters, and a secondary clock that is used only by one specified filter.




## -parameters




### -param pClockForMostOfFilterGraph [in]

Pointer to the <a href="https://msdn.microsoft.com/9818c67d-dfbe-4498-a744-d2efaa4bfb58">IReferenceClock</a> interface of the main reference clock. Every filter in the graph uses this clock, except for the filter specified by the <i>pFilter</i> parameter.


### -param pClockForFilter [in]

Pointer to the <b>IReferenceClock</b> interface of the secondary clock. The filter specified by the <i>pFilter</i> parameter uses this clock.


### -param pFilter [in]

Pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of a filter in the graph. This filter uses the secondary reference clock.


## -returns



Returns and <b>HRESULT</b> value. Possible values include the following.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is not stopped.

</td>
</tr>
</table>
 




## -remarks



If the filter graph is running or paused, this method return VFW_E_NOT_STOPPED.

To clear both reference clocks, set all three parameters to <b>NULL</b>. To set a single clock for the entire graph, with no secondary clock, call the <a href="https://msdn.microsoft.com/a374c963-cc28-41f6-814d-7ffc6efc67a6">IMediaFilter::SetSyncSource</a> method on the Filter Graph Manager.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1d5f8eda-2b09-4627-8ae9-f43f38c3c26a">IFilterGraph3 Interface</a>
 

 

