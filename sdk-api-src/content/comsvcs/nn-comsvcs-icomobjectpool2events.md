---
UID: NN:comsvcs.IComObjectPool2Events
title: IComObjectPool2Events (comsvcs.h)
author: windows-sdk-content
description: Notifies the subscriber if a transactional or non-transactional object is added to or obtained from the object pool.
old-location: cos\icomobjectpool2events.htm
tech.root: cossdk
ms.assetid: 2aac494d-52ce-408c-8444-8792b5b53604
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComObjectPool2Events, IComObjectPool2Events interface [COM+], IComObjectPool2Events interface [COM+],described, _dtc_icomobjectpool2events, comsvcs/IComObjectPool2Events, cos.icomobjectpool2events
ms.topic: interface
f1_keywords: ["comsvcs/IComObjectPool2Events"]
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
 - IComObjectPool2Events
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComObjectPool2Events interface


## -description


Notifies the subscriber if a transactional or non-transactional object is added to or obtained from the object pool. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectPool2Events</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComObjectPool2Events</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectpool2events-onobjpoolgetfromtx2">OnObjPoolGetFromTx2</a>
</td>
<td align="left" width="63%">
Generated when a transactional object is obtained from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectpool2events-onobjpoolgetobject2">OnObjPoolGetObject2</a>
</td>
<td align="left" width="63%">
Generated when a non-transactional object is obtained from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectpool2events-onobjpoolputobject2">OnObjPoolPutObject2</a>
</td>
<td align="left" width="63%">
Generated when an object is added to the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectpool2events-onobjpoolrecycletotx2">OnObjPoolRecycleToTx2</a>
</td>
<td align="left" width="63%">
Generated when a transactional object is returned to the pool.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

