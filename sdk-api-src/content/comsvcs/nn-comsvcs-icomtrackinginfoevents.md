---
UID: NN:comsvcs.IComTrackingInfoEvents
title: IComTrackingInfoEvents (comsvcs.h)
description: Notifies the subscriber when the tracking information for a collection changes.
old-location: cos\icomtrackinginfoevents.htm
tech.root: cossdk
ms.assetid: bed709ca-5083-4073-a9f9-2b7b7f14cf87
ms.date: 12/05/2018
ms.keywords: IComTrackingInfoEvents, IComTrackingInfoEvents interface [COM+], IComTrackingInfoEvents interface [COM+],described, _dtc_IComTrackingInfoEvents, comsvcs/IComTrackingInfoEvents, cos.icomtrackinginfoevents
ms.topic: interface
f1_keywords:
- comsvcs/IComTrackingInfoEvents
dev_langs:
- c++
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- IComTrackingInfoEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComTrackingInfoEvents interface


## -description


Notifies the subscriber when the tracking information for a collection changes. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComTrackingInfoEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComTrackingInfoEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComTrackingInfoEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomtrackinginfoevents-onnewtrackinginfo">OnNewTrackingInfo</a>
</td>
<td align="left" width="63%">
Generated when the tracking information for a collection changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

