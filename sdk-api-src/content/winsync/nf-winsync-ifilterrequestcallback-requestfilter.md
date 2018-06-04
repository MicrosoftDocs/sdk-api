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

# IFilterRequestCallback::RequestFilter


## -description


Requests that the filter that is specified by the destination provider be used by the source provider during change enumeration.


## -parameters




### -param pFilter [in]

The filter that is specified by the destination provider. This filter is passed to the source provider to be used during change enumeration.


### -param filteringType [in]

A <a href="https://msdn.microsoft.com/6bcbc011-9d47-4c88-a62e-0c9366abc7d3">FILTERING_TYPE</a> enumeration value that indicates the type of information that is included in a change batch during filtered synchronization.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_FILTER_NOT_SUPPPORTED</b></dt>
</dl>
</td>
<td width="60%">
When the filter that is specified by <i>pFilter</i> is not supported by the source provider. This is also returned when the source provider does not implement <a href="https://msdn.microsoft.com/cf07e322-7c75-49a4-a514-b4c782ceb2d7">ISupportFilteredSync</a>.

</td>
</tr>
</table>
 




## -remarks



Filter negotiation is achieved by using the following steps:

<ol>
<li>Before the source provider begins enumerating changes, starts filter negotiation by calling <a href="https://msdn.microsoft.com/653e953f-3f08-4d65-85d5-3c5466361ea5">IRequestFilteredSync::SpecifyFilter</a> on the destination provider.</li>
<li>During processing of <a href="https://msdn.microsoft.com/653e953f-3f08-4d65-85d5-3c5466361ea5">IRequestFilteredSync::SpecifyFilter</a>, the destination provider passes filters to <b>IFilterRequestCallback::RequestFilter</b>.</li>
<li>During processing of <b>IFilterRequestCallback::RequestFilter</b>, calls <a href="https://msdn.microsoft.com/00a533fa-2a91-46e8-9754-af162a5e59ec">ISupportFilteredSync::AddFilter</a> on the source provider. If the source provider does not support the requested filter, the destination provider can continue to request filters until it finds one that is supported.</li>
</ol>
When a filter has been successfully negotiated, the source provider uses it to determine which items to include during change enumeration.




## -see-also




<a href="https://msdn.microsoft.com/6bcbc011-9d47-4c88-a62e-0c9366abc7d3">FILTERING_TYPE Enumeration</a>



<a href="https://msdn.microsoft.com/11ba822e-63d6-4947-8e21-7134bdbcbdc0">IFilterRequestCallback Interface</a>



<a href="https://msdn.microsoft.com/e4b76bb3-d572-4441-94db-7088e881ede2">IRequestFilteredSync Interface</a>



<a href="https://msdn.microsoft.com/cf07e322-7c75-49a4-a514-b4c782ceb2d7">ISupportFilteredSync Interface</a>
 

 

