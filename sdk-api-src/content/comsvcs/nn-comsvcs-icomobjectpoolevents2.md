---
UID: NN:comsvcs.IComObjectPoolEvents2
title: IComObjectPoolEvents2
author: windows-sdk-content
description: Notifies the subscriber when a new object is created for or removed from the pool.
old-location: cos\icomobjectpoolevents2.htm
tech.root: cossdk
ms.assetid: f1891d8b-e3d0-4378-ac67-c2c0ddd65602
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComObjectPoolEvents2, IComObjectPoolEvents2 interface [COM+], IComObjectPoolEvents2 interface [COM+],described, _dtc_IComObjectPoolEvents2, comsvcs/IComObjectPoolEvents2, cos.icomobjectpoolevents2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComObjectPoolEvents2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComObjectPoolEvents2 interface


## -description


Notifies the subscriber when a new object is created for or removed from the pool. The subscriber is also notified when a new object pool is created or when the request for a pooled object times out. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectPoolEvents2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComObjectPoolEvents2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComObjectPoolEvents2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a66c00ac-b9b9-431e-b1c8-6642cb35ec3c">OnObjPoolCreateDecision</a>
</td>
<td align="left" width="63%">
Generated when a pool provides a requesting client with an existing object or creates a new one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85e50bf4-2660-409c-8812-cbe389283202">OnObjPoolCreateObject</a>
</td>
<td align="left" width="63%">
Generated when an object is created for the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa7a5ee4-8304-426c-9063-d25e2ed69668">OnObjPoolCreatePool</a>
</td>
<td align="left" width="63%">
Generated when a new pool is created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c942da45-4d41-4483-a30b-862d3e0c13b7">OnObjPoolDestroyObject</a>
</td>
<td align="left" width="63%">
Generated when an object is permanently removed from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5468ae6-6c7e-4ae1-afbc-24cc9b08102f">OnObjPoolTimeout</a>
</td>
<td align="left" width="63%">
Generated when the request for a pooled object times out.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

