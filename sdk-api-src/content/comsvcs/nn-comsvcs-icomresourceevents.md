---
UID: NN:comsvcs.IComResourceEvents
title: IComResourceEvents
author: windows-sdk-content
description: Notifies the subscriber if a resource is created, allocated, tracked, or destroyed.
old-location: cos\icomresourceevents.htm
old-project: cossdk
ms.assetid: fdc664b6-0459-4cbd-8e9e-0c3fe82e4321
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IComResourceEvents, IComResourceEvents interface [COM+], IComResourceEvents interface [COM+],described, _dtc_IComResourceEvents, comsvcs/IComResourceEvents, cos.icomresourceevents
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
 - IComResourceEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComResourceEvents interface


## -description


Notifies the subscriber if a resource is created, allocated, tracked, or destroyed. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComResourceEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComResourceEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComResourceEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f063230d-a0b8-46c5-845c-f94aefb706a7">OnResourceAllocate</a>
</td>
<td align="left" width="63%">
Generated when an existing resource is allocated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c1cb030-c6c7-4f91-a1ea-eebbec41813b">OnResourceCreate</a>
</td>
<td align="left" width="63%">
Generated when a new resource is created and allocated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc934b47-8031-4dab-ae00-6389f54749b8">OnResourceDestroy</a>
</td>
<td align="left" width="63%">
Generated when a resource is destroyed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/615e0f73-2935-4ef3-94c9-5c74b5c82db4">OnResourceRecycle</a>
</td>
<td align="left" width="63%">
Generated when an object is finished with a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8845cf07-f796-45bd-9d3d-261cf0903050">OnResourceTrack</a>
</td>
<td align="left" width="63%">
Generated when a resource is tracked.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

