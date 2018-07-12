---
UID: NN:comsvcs.IComObjectPoolEvents
title: IComObjectPoolEvents
author: windows-sdk-content
description: Notifies the subscriber when a new object is added to the pool.
old-location: cos\icomobjectpoolevents.htm
old-project: cossdk
ms.assetid: a830b40b-a1b1-464e-b532-91cebd4e5d2f
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: IComObjectPoolEvents, IComObjectPoolEvents interface [COM+], IComObjectPoolEvents interface [COM+],described, _dtc_IComObjectPoolEvents, comsvcs/IComObjectPoolEvents, cos.icomobjectpoolevents
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComObjectPoolEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComObjectPoolEvents interface


## -description


Notifies the subscriber when a new object is added to the pool. The subscriber is also notified when a transactional or non-transactional object is obtained or returned to the pool. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectPoolEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComObjectPoolEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComObjectPoolEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/977ab640-a9d5-47f5-ad47-ad2e1648fd6b">OnObjPoolGetFromTx</a>
</td>
<td align="left" width="63%">
Generated when a transactional object is obtained from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/532575b4-af72-4b53-b90b-fc09966c8ee0">OnObjPoolGetObject</a>
</td>
<td align="left" width="63%">
Generated when a non-transactional object is obtained from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00b0b3b1-943d-4fba-bd5d-52d6de80fcf6">OnObjPoolPutObject</a>
</td>
<td align="left" width="63%">
Generated when a new object is added to the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6acae10b-9fda-4c73-b781-62a480271fd1">OnObjPoolRecycleToTx</a>
</td>
<td align="left" width="63%">
Generated when a transactional object is returned to the pool.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

