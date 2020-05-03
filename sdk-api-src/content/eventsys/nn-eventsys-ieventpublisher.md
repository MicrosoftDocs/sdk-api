---
UID: NN:eventsys.IEventPublisher
title: IEventPublisher (eventsys.h)
description: Registers, modifies, removes, and provides information about an event publisher.helpviewer_keywords: ["IEventPublisher","IEventPublisher interface [COM]","IEventPublisher interface [COM]","described","_com_ieventpublisher","com.ieventpublisher","eventsys/IEventPublisher"]
old-location: com\ieventpublisher.htm
tech.root: com
ms.assetid: 132b79c8-d7f4-49c1-87c7-9bdf311ae697
ms.date: 12/05/2018
ms.keywords: IEventPublisher, IEventPublisher interface [COM], IEventPublisher interface [COM],described, _com_ieventpublisher, com.ieventpublisher, eventsys/IEventPublisher
f1_keywords:
- eventsys/IEventPublisher
dev_langs:
- c++
req.header: eventsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EventSys.idl
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
- EventSys.h
api_name:
- IEventPublisher
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventPublisher interface


## -description


Registers, modifies, removes, and provides information about an event publisher.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventPublisher</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEventPublisher</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IEventPublisher</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventpublisher-getdefaultproperty">GetDefaultProperty</a>
</td>
<td align="left" width="63%">
Retrieves a named property and its value from the property bag associated with the event publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventpublisher-getdefaultpropertycollection">GetDefaultPropertyCollection</a>
</td>
<td align="left" width="63%">
Creates a collection object that enumerates the properties contained in the property bag associated with the event publisher object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventpublisher-putdefaultproperty">PutDefaultProperty</a>
</td>
<td align="left" width="63%">
Writes a named property and its value to the property bag associated with the event publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventpublisher-removedefaultproperty">RemoveDefaultProperty</a>
</td>
<td align="left" width="63%">
Removes a named property and its value from the property bag associated with the event publisher object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventPublisher</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventpublisher-get_description">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The display text for the event publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventpublisher-get_ownersid">OwnerSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The security identifier of the creator of the event publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventpublisher-put_publisherid">PublisherID</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
The identifier for the event publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventpublisher-get_publishername">PublisherName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The display name for the event publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventpublisher-get_publishertype">PublisherType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The optional administrative group for the event publisher.

</td>
</tr>
</table> 

