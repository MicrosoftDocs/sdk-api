---
UID: NN:comsvcs.IComObjectPool2Events
title: IComObjectPool2Events
author: windows-sdk-content
description: Notifies the subscriber if a transactional or non-transactional object is added to or obtained from the object pool.
old-location: cos\icomobjectpool2events.htm
old-project: cossdk
ms.assetid: 2aac494d-52ce-408c-8444-8792b5b53604
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IComObjectPool2Events, IComObjectPool2Events interface [COM+], IComObjectPool2Events interface [COM+],described, _dtc_icomobjectpool2events, comsvcs/IComObjectPool2Events, cos.icomobjectpool2events
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
 - IComObjectPool2Events
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComObjectPool2Events interface


## -description


Notifies the subscriber if a transactional or non-transactional object is added to or obtained from the object pool. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectPool2Events</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComObjectPool2Events</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComObjectPool2Events</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1c8b02a-8262-48f6-a160-5bef21bed5ce">OnObjPoolGetFromTx2</a>
</td>
<td align="left" width="63%">
Generated when a transactional object is obtained from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/322540f2-7f99-41ad-b6b5-59067f350feb">OnObjPoolGetObject2</a>
</td>
<td align="left" width="63%">
Generated when a non-transactional object is obtained from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a0cfbd2-d88c-4773-96e5-0e97767d647d">OnObjPoolPutObject2</a>
</td>
<td align="left" width="63%">
Generated when an object is added to the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f737289f-c990-455e-bc9b-e94f25c9297f">OnObjPoolRecycleToTx2</a>
</td>
<td align="left" width="63%">
Generated when a transactional object is returned to the pool.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

