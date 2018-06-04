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

# IFilterGraph::RemoveFilter


## -description



The <code>RemoveFilter</code> method removes a filter from the graph.




## -parameters




### -param pFilter [in]

Pointer to the filter to be removed from the graph.


## -returns



Returns one of the following values.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



The Filter Graph Manager notifies the filter that it is being removed by calling the filter's <a href="https://msdn.microsoft.com/1f01c71f-5c12-4bf3-937c-740168baf776">IBaseFilter::JoinFilterGraph</a> method with a <b>NULL</b> argument. It is not necessary to disconnect the filter's pins before calling <code>RemoveFilter</code>, but the filter graph should be in the Stopped state. If the filters are not stopped, <code>RemoveFilter</code> may fail to disconnect the pins and then fail to remove the filter from the graph. <a href="https://msdn.microsoft.com/c3298aa2-4eb2-4e47-9f36-5f2cf541d13e">IGraphConfig::RemoveFilterEx</a> enables an application to remove a filter without disconnecting the pins automatically, which improves performance if you want to move groups of connected filters into a new graph.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph Interface</a>
 

 

