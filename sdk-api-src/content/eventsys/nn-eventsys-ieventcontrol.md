---
UID: NN:eventsys.IEventControl
title: IEventControl
author: windows-sdk-content
description: Controls the behavior of an event object, the object that fires an event to its subscribers.
old-location: cos\ieventcontrol.htm
tech.root: cossdk
ms.assetid: 8b2fba30-3ede-466f-ad3b-2de2175a088b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IEventControl, IEventControl interface [COM+], IEventControl interface [COM+],described, _cos_IEventControl, cos.ieventcontrol, eventsys/IEventControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Eventsys.idl
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
 - Eventsys.h
api_name:
 - IEventControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEventControl interface


## -description


Controls the behavior of an event object, the object that fires an event to its subscribers.

The <b>IEventControl</b> interface differs from the <a href="https://msdn.microsoft.com/e603f68a-881c-468d-a3d3-738f43400e01">IMultiInterfaceEventControl</a> interface in that it supports only one interface for the event object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventControl</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IEventControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IEventControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba39305d-8dc3-40fe-b6f6-d5c22f54a180">GetSubscriptions</a>
</td>
<td align="left" width="63%">
Retrieves the collection of subscriptions associated with an event method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea0cc4b8-e345-44bc-969e-f35f25b641f9">SetDefaultQuery</a>
</td>
<td align="left" width="63%">
Sets the default query to determine subscribers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ebe0f55-9e2f-4538-9c16-1b237abfd07b">SetPublisherFilter</a>
</td>
<td align="left" width="63%">
Assigns a publisher filter to an event method.


</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventControl</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bbb6c514-8eb0-4e5e-a23e-d4857786cfd3">AllowInprocActivation</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether subscribers can be activated in the publisher's process.

</td>
</tr>
</table> 

