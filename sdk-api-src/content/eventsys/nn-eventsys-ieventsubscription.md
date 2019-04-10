---
UID: NN:eventsys.IEventSubscription
title: IEventSubscription (eventsys.h)
author: windows-sdk-content
description: Specifies information about the relationship between an event subscriber and an event to which it is subscribing. It is used by publisher filters.
old-location: cos\ieventsubscription.htm
tech.root: cossdk
ms.assetid: ce3f9f7e-3d0a-445f-b3db-671ee595aedf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEventSubscription, IEventSubscription interface [COM+], IEventSubscription interface [COM+],described, _cos_IEventSubscription, cos.ieventsubscription, eventsys/IEventSubscription
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
 - IEventSubscription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEventSubscription interface


## -description


Specifies information about the relationship between an event subscriber and an event to which it is subscribing.
It is used by publisher filters.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventSubscription</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IEventSubscription</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7d0c2467-0ab8-4daf-b4ed-befe28d33757">GetPublisherProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property stored in the property bag to define publisher context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d59b46bc-cfc4-400b-8b91-6d0f68f8d9b3">GetPublisherPropertyCollection</a>
</td>
<td align="left" width="63%">
Retrieves a collection of properties and values stored in the publisher property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e16557a-e4ea-46ae-8285-0446189cea8e">GetSubscriberProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property stored in the property bag to define subscriber context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33d00424-a285-4953-aa96-be30d3e7da17">GetSubscriberPropertyCollection</a>
</td>
<td align="left" width="63%">
Retrieves a collection of properties and values stored in the subscriber property bag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af8ae243-d28b-4909-a4e8-98ffe336fc9a">PutPublisherProperty</a>
</td>
<td align="left" width="63%">
Writes a property and its value to the property bag to define publisher context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/817ee07c-32ea-41a4-a871-370c06bfc8a8">PutSubscriberProperty</a>
</td>
<td align="left" width="63%">
Writes a property and its value to the property bag to define subscriber context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3893e605-dd01-47d3-bb7d-095964433ef9">RemovePublisherProperty</a>
</td>
<td align="left" width="63%">
Removes a property and its value from the property bag that defines publisher context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c0cd763-8528-4f8b-8a09-c36860cad9b7">RemoveSubscriberProperty</a>
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

<a href="https://msdn.microsoft.com/59648682-12c4-4c55-83f6-57c6ec5d6d02">Description</a>


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

<a href="https://msdn.microsoft.com/02481b3d-1064-448f-955b-0dd02d90db46">Enabled</a>


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

<a href="https://msdn.microsoft.com/cba78857-0b59-4012-84d6-f5e7ae28b8bd">EventClassID</a>


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

<a href="https://msdn.microsoft.com/13e88201-98c3-476e-bc75-34aed0b9ce9e">InterfaceID</a>


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

<a href="https://msdn.microsoft.com/b56027ac-abe6-4d13-ad3a-254a2f92ab6d">MachineName</a>


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

<a href="https://msdn.microsoft.com/2959e1f3-5b16-40a3-abdf-7fe18be2336b">MethodName</a>


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

<a href="https://msdn.microsoft.com/ab914aa3-04fc-424e-b799-c6268c014080">OwnerSID</a>


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

<a href="https://msdn.microsoft.com/2247213f-6458-4d09-8fa3-2ac90c52b711">PerUser</a>


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

<a href="https://msdn.microsoft.com/94f335be-aeb5-4d24-b475-e2aaae2b0a17">PublisherID</a>


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

<a href="https://msdn.microsoft.com/004f662c-8fcb-4490-897b-48bf5ea306c7">SubscriberCLSID</a>


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

<a href="https://msdn.microsoft.com/207c8e74-d8f8-4576-8f2d-762c97bc048f">SubscriberInterface</a>


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

<a href="https://msdn.microsoft.com/923eadb6-2ee8-4db9-952a-69f73367b2f8">SubscriptionID</a>


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

<a href="https://msdn.microsoft.com/0a5532c1-8e06-4fbd-88aa-04d7a69672c3">SubscriptionName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
A displayable name for the subscription object.

</td>
</tr>
</table> 

