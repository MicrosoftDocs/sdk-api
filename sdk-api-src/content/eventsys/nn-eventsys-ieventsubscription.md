---
UID: NN:eventsys.IEventSubscription
title: IEventSubscription (eventsys.h)
description: Specifies information about the relationship between an event subscriber and an event to which it is subscribing. It is used by publisher filters.
helpviewer_keywords: ["IEventSubscription","IEventSubscription interface [COM+]","IEventSubscription interface [COM+]","described","_cos_IEventSubscription","cos.ieventsubscription","eventsys/IEventSubscription"]
old-location: cos\ieventsubscription.htm
tech.root: cos
ms.assetid: ce3f9f7e-3d0a-445f-b3db-671ee595aedf
ms.date: 12/05/2018
ms.keywords: IEventSubscription, IEventSubscription interface [COM+], IEventSubscription interface [COM+],described, _cos_IEventSubscription, cos.ieventsubscription, eventsys/IEventSubscription
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEventSubscription
 - eventsys/IEventSubscription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EventSys.h
api_name:
 - IEventSubscription
---

# IEventSubscription interface


## -description

Specifies information about the relationship between an event subscriber and an event to which it is subscribing.
It is used by publisher filters.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventSubscription</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEventSubscription</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IEventSubscription</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-getpublisherproperty">GetPublisherProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property stored in the property bag to define publisher context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-getpublisherpropertycollection">GetPublisherPropertyCollection</a>
</td>
<td align="left" width="63%">
Retrieves a collection of properties and values stored in the publisher property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-getsubscriberproperty">GetSubscriberProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property stored in the property bag to define subscriber context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-getsubscriberpropertycollection">GetSubscriberPropertyCollection</a>
</td>
<td align="left" width="63%">
Retrieves a collection of properties and values stored in the subscriber property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putpublisherproperty">PutPublisherProperty</a>
</td>
<td align="left" width="63%">
Writes a property and its value to the property bag to define publisher context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-putsubscriberproperty">PutSubscriberProperty</a>
</td>
<td align="left" width="63%">
Writes a property and its value to the property bag to define subscriber context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-removepublisherproperty">RemovePublisherProperty</a>
</td>
<td align="left" width="63%">
Removes a property and its value from the property bag that defines publisher context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-removesubscriberproperty">RemoveSubscriberProperty</a>
</td>
<td align="left" width="63%">
Removes a property and its value from the property bag that defines subscriber context.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventSubscription</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_description">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
A displayable text description of the subscription.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_enabled">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the subscription is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_eventclassid">EventClassID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The unique ID of the event class associated with the subscription.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_interfaceid">InterfaceID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The identifier for a particular interface for which the subscriber wants to receive events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_machinename">MachineName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The name of the computer on which the subscriber should be activated (for a persistent subscription).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_methodname">MethodName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The name of the event method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_ownersid">OwnerSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The security ID of the subscription's creator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_peruser">PerUser</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Indicates whether the subscription receives the event only if the owner of the subscription is logged on to the same computer as the publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_publisherid">PublisherID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The unique ID of the event publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_subscriberclsid">SubscriberCLSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The CLSID of the subscriber component (for a persistent subscription).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_subscriberinterface">SubscriberInterface</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
A marshaled pointer to the event interface on the subscriber (for a transient subscription).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_subscriptionid">SubscriptionID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The unique ID for the subscription object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsubscription-get_subscriptionname">SubscriptionName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
A displayable name for the subscription object.

</td>
</tr>
</table>

