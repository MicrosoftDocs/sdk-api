---
UID: NN:comsvcs.IComResourceEvents
title: IComResourceEvents (comsvcs.h)
description: Notifies the subscriber if a resource is created, allocated, tracked, or destroyed.
helpviewer_keywords: ["IComResourceEvents","IComResourceEvents interface [COM+]","IComResourceEvents interface [COM+]","described","_dtc_IComResourceEvents","comsvcs/IComResourceEvents","cos.icomresourceevents"]
old-location: cos\icomresourceevents.htm
tech.root: cossdk
ms.assetid: fdc664b6-0459-4cbd-8e9e-0c3fe82e4321
ms.date: 12/05/2018
ms.keywords: IComResourceEvents, IComResourceEvents interface [COM+], IComResourceEvents interface [COM+],described, _dtc_IComResourceEvents, comsvcs/IComResourceEvents, cos.icomresourceevents
f1_keywords:
- comsvcs/IComResourceEvents
dev_langs:
- c++
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
- IComResourceEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComResourceEvents interface


## -description


Notifies the subscriber if a resource is created, allocated, tracked, or destroyed. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComResourceEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComResourceEvents</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomresourceevents-onresourceallocate">OnResourceAllocate</a>
</td>
<td align="left" width="63%">
Generated when an existing resource is allocated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomresourceevents-onresourcecreate">OnResourceCreate</a>
</td>
<td align="left" width="63%">
Generated when a new resource is created and allocated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomresourceevents-onresourcedestroy">OnResourceDestroy</a>
</td>
<td align="left" width="63%">
Generated when a resource is destroyed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomresourceevents-onresourcerecycle">OnResourceRecycle</a>
</td>
<td align="left" width="63%">
Generated when an object is finished with a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomresourceevents-onresourcetrack">OnResourceTrack</a>
</td>
<td align="left" width="63%">
Generated when a resource is tracked.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

