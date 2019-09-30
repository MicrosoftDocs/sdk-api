---
UID: NN:comsvcs.IComObjectPoolEvents
title: IComObjectPoolEvents (comsvcs.h)
author: windows-sdk-content
description: Notifies the subscriber when a new object is added to the pool.
old-location: cos\icomobjectpoolevents.htm
tech.root: cossdk
ms.assetid: a830b40b-a1b1-464e-b532-91cebd4e5d2f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComObjectPoolEvents, IComObjectPoolEvents interface [COM+], IComObjectPoolEvents interface [COM+],described, _dtc_IComObjectPoolEvents, comsvcs/IComObjectPoolEvents, cos.icomobjectpoolevents
ms.topic: interface
f1_keywords: 
 - "comsvcs/IComObjectPoolEvents"
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
 - IComObjectPoolEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComObjectPoolEvents interface


## -description


Notifies the subscriber when a new object is added to the pool. The subscriber is also notified when a transactional or non-transactional object is obtained or returned to the pool. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectPoolEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComObjectPoolEvents</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectpoolevents-onobjpoolgetfromtx">OnObjPoolGetFromTx</a>
</td>
<td align="left" width="63%">
Generated when a transactional object is obtained from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectpoolevents-onobjpoolgetobject">OnObjPoolGetObject</a>
</td>
<td align="left" width="63%">
Generated when a non-transactional object is obtained from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectpoolevents-onobjpoolputobject">OnObjPoolPutObject</a>
</td>
<td align="left" width="63%">
Generated when a new object is added to the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomobjectpoolevents-onobjpoolrecycletotx">OnObjPoolRecycleToTx</a>
</td>
<td align="left" width="63%">
Generated when a transactional object is returned to the pool.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

