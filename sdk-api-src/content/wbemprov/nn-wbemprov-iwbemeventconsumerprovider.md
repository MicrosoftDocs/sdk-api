---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWbemEventConsumerProvider interface


## -description


The 
<b>IWbemEventConsumerProvider</b> interface provides the primary interface for an event consumer provider. Through 
this interface and the 
<a href="https://msdn.microsoft.com/196c839a-5b8f-4ff6-b6cf-3483db275e8b">FindConsumer</a> method, an event consumer provider can indicate which event consumers should receive a given event. The first time WMI delivers an event to a particular consumer, WMI calls 
<a href="https://msdn.microsoft.com/196c839a-5b8f-4ff6-b6cf-3483db275e8b">FindConsumer</a> to retrieve a pointer to the sink for that physical consumer. WMI then sends all subsequent occurrences of the event the sink provided by 
<b>FindConsumer</b>.

If you implement a permanent event consumer, you must implement 
<b>IWbemEventConsumerProvider</b> so that WMI can deliver events to your physical consumer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemEventConsumerProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemEventConsumerProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemEventConsumerProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/196c839a-5b8f-4ff6-b6cf-3483db275e8b">FindConsumer</a>
</td>
<td align="left" width="63%">
Called by Windows Management to retrieve an 
<a href="https://msdn.microsoft.com/a890aefe-e35e-4635-874d-953194f99a82">IWbemUnboundObjectSink</a> object for a particular logical consumer.

</td>
</tr>
</table> 

