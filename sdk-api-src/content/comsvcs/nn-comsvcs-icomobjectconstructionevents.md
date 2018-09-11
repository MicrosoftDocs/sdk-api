---
UID: NN:comsvcs.IComObjectConstructionEvents
title: IComObjectConstructionEvents
author: windows-sdk-content
description: Notifies the subscriber if a constructed object is created in an object pool.
old-location: cos\icomobjectconstructionevents.htm
tech.root: cossdk
ms.assetid: c5fdb9b1-937e-43cb-93ff-e90f8c268fee
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComObjectConstructionEvents, IComObjectConstructionEvents interface [COM+], IComObjectConstructionEvents interface [COM+],described, _dtc_IComObjectConstructionEvents, comsvcs/IComObjectConstructionEvents, cos.icomobjectconstructionevents
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
 - IComObjectConstructionEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComObjectConstructionEvents interface


## -description


Notifies the subscriber if a constructed object is created in an object pool. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog. A constructed object is derived from the <a href="https://msdn.microsoft.com/en-us/library/ms680583(v=VS.85).aspx">IObjectConstruct</a> interface. Constructed objects can inherit parameter names from within other objects or libraries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectConstructionEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IComObjectConstructionEvents</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IComObjectConstructionEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683644(v=VS.85).aspx">OnObjectConstruct</a>
</td>
<td align="left" width="63%">
Generated when a constructed object is created.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678896(v=VS.85).aspx">COM+ Instrumentation</a>
 

 

