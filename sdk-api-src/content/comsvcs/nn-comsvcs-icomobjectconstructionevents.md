---
UID: NN:comsvcs.IComObjectConstructionEvents
title: IComObjectConstructionEvents (comsvcs.h)
author: windows-sdk-content
description: Notifies the subscriber if a constructed object is created in an object pool.
old-location: cos\icomobjectconstructionevents.htm
tech.root: cossdk
ms.assetid: c5fdb9b1-937e-43cb-93ff-e90f8c268fee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComObjectConstructionEvents, IComObjectConstructionEvents interface [COM+], IComObjectConstructionEvents interface [COM+],described, _dtc_IComObjectConstructionEvents, comsvcs/IComObjectConstructionEvents, cos.icomobjectconstructionevents
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


Notifies the subscriber if a constructed object is created in an object pool. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog. A constructed object is derived from the <a href="https://msdn.microsoft.com/3fc84c37-f38d-4ff1-bdb1-f5d298802b64">IObjectConstruct</a> interface. Constructed objects can inherit parameter names from within other objects or libraries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectConstructionEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComObjectConstructionEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/8a90e561-79a0-4490-bbc8-f376e4278ab9">OnObjectConstruct</a>
</td>
<td align="left" width="63%">
Generated when a constructed object is created.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

