---
UID: NN:comsvcs.IComObjectPoolEvents2
title: IComObjectPoolEvents2
author: windows-sdk-content
description: Notifies the subscriber when a new object is created for or removed from the pool.
old-location: cos\icomobjectpoolevents2.htm
tech.root: cossdk
ms.assetid: f1891d8b-e3d0-4378-ac67-c2c0ddd65602
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComObjectPoolEvents2, IComObjectPoolEvents2 interface [COM+], IComObjectPoolEvents2 interface [COM+],described, _dtc_IComObjectPoolEvents2, comsvcs/IComObjectPoolEvents2, cos.icomobjectpoolevents2
ms.prod: windows-hardware
ms.technology: windows-devices
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


Notifies the subscriber when a new object is created for or removed from the pool. The subscriber is also notified when a new object pool is created or when the request for a pooled object times out. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectPoolEvents2</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IComObjectPoolEvents2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms685162(v=VS.85).aspx">OnObjPoolCreateDecision</a>
</td>
<td align="left" width="63%">
Generated when a pool provides a requesting client with an existing object or creates a new one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683584(v=VS.85).aspx">OnObjPoolCreateObject</a>
</td>
<td align="left" width="63%">
Generated when an object is created for the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms688436(v=VS.85).aspx">OnObjPoolCreatePool</a>
</td>
<td align="left" width="63%">
Generated when a new pool is created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686458(v=VS.85).aspx">OnObjPoolDestroyObject</a>
</td>
<td align="left" width="63%">
Generated when an object is permanently removed from the pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685123(v=VS.85).aspx">OnObjPoolTimeout</a>
</td>
<td align="left" width="63%">
Generated when the request for a pooled object times out.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678896(v=VS.85).aspx">COM+ Instrumentation</a>
 

 

