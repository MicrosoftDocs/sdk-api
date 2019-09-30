---
UID: NN:eventsys.IEventControl
title: IEventControl (eventsys.h)
author: windows-sdk-content
description: Controls the behavior of an event object, the object that fires an event to its subscribers.
old-location: cos\ieventcontrol.htm
tech.root: cossdk
ms.assetid: 8b2fba30-3ede-466f-ad3b-2de2175a088b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEventControl, IEventControl interface [COM+], IEventControl interface [COM+],described, _cos_IEventControl, cos.ieventcontrol, eventsys/IEventControl
ms.topic: interface
f1_keywords: 
 - "eventsys/IEventControl"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventControl interface


## -description


Controls the behavior of an event object, the object that fires an event to its subscribers.

The <b>IEventControl</b> interface differs from the <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-imultiinterfaceeventcontrol">IMultiInterfaceEventControl</a> interface in that it supports only one interface for the event object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventControl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEventControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventcontrol-getsubscriptions">GetSubscriptions</a>
</td>
<td align="left" width="63%">
Retrieves the collection of subscriptions associated with an event method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventcontrol-setdefaultquery">SetDefaultQuery</a>
</td>
<td align="left" width="63%">
Sets the default query to determine subscribers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventcontrol-setpublisherfilter">SetPublisherFilter</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventcontrol-get_allowinprocactivation">AllowInprocActivation</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether subscribers can be activated in the publisher's process.

</td>
</tr>
</table> 

