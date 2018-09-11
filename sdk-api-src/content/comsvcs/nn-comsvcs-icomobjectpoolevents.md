---
UID: NN:comsvcs.IComObjectPoolEvents
title: IComObjectPoolEvents
author: windows-sdk-content
description: Notifies the subscriber when a new object is added to the pool.
old-location: cos\icomobjectpoolevents.htm
tech.root: cossdk
ms.assetid: a830b40b-a1b1-464e-b532-91cebd4e5d2f
ms.author: windowssdkdev
ms.date: 08/29/2018
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComObjectPoolEvents interface


## -description


Notifies the subscriber when a new object is added to the pool. The subscriber is also notified when a transactional or non-transactional object is obtained or returned to the pool. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectPoolEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IComObjectPoolEvents</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms684307(v=VS.85).aspx">OnObjPoolGetFromTx</a>
</td>
<td align="left" width="63%">
Generated when a transactional object is obtained from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681300(v=VS.85).aspx">OnObjPoolGetObject</a>
</td>
<td align="left" width="63%">
Generated when a non-transactional object is obtained from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678826(v=VS.85).aspx">OnObjPoolPutObject</a>
</td>
<td align="left" width="63%">
Generated when a new object is added to the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682217(v=VS.85).aspx">OnObjPoolRecycleToTx</a>
</td>
<td align="left" width="63%">
Generated when a transactional object is returned to the pool.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678896(v=VS.85).aspx">COM+ Instrumentation</a>
 

 

