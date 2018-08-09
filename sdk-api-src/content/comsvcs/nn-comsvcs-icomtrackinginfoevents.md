---
UID: NN:comsvcs.IComTrackingInfoEvents
title: IComTrackingInfoEvents
author: windows-sdk-content
description: Notifies the subscriber when the tracking information for a collection changes.
old-location: cos\icomtrackinginfoevents.htm
old-project: cossdk
ms.assetid: bed709ca-5083-4073-a9f9-2b7b7f14cf87
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IComTrackingInfoEvents, IComTrackingInfoEvents interface [COM+], IComTrackingInfoEvents interface [COM+],described, _dtc_IComTrackingInfoEvents, comsvcs/IComTrackingInfoEvents, cos.icomtrackinginfoevents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IComTrackingInfoEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComTrackingInfoEvents interface


## -description


Notifies the subscriber when the tracking information for a collection changes. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComTrackingInfoEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComTrackingInfoEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a63f6782-b50a-4457-bd51-4eba8c413a47">OnNewTrackingInfo</a>
</td>
<td align="left" width="63%">
Generated when the tracking information for a collection changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

