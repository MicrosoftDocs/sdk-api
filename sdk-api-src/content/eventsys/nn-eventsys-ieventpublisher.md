---
UID: NN:eventsys.IEventPublisher
title: IEventPublisher
author: windows-sdk-content
description: Registers, modifies, removes, and provides information about an event publisher.
old-location: com\ieventpublisher.htm
tech.root: com
ms.assetid: 132b79c8-d7f4-49c1-87c7-9bdf311ae697
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IEventPublisher, IEventPublisher interface [COM], IEventPublisher interface [COM],described, _com_ieventpublisher, com.ieventpublisher, eventsys/IEventPublisher
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEventPublisher interface


## -description


Registers, modifies, removes, and provides information about an event publisher.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventPublisher</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IEventPublisher</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5d9adc4f-30c9-42bd-89c9-e35384885b8c">GetDefaultProperty</a>
</td>
<td align="left" width="63%">
Retrieves a named property and its value from the property bag associated with the event publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca5d116a-b995-4311-9c58-6b957fca6b53">GetDefaultPropertyCollection</a>
</td>
<td align="left" width="63%">
Creates a collection object that enumerates the properties contained in the property bag associated with the event publisher object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/418f1c16-1b21-4023-b0fc-6e9082b8264e">PutDefaultProperty</a>
</td>
<td align="left" width="63%">
Writes a named property and its value to the property bag associated with the event publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da691bac-e940-431d-acef-8c29f4a25c70">RemoveDefaultProperty</a>
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

<a href="https://msdn.microsoft.com/1fead633-e498-4dc2-8591-d1f9c0090adb">Description</a>


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

<a href="https://msdn.microsoft.com/7555992f-ba50-4d3e-afa8-6304fec8b5c5">OwnerSID</a>


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

<a href="https://msdn.microsoft.com/edc66367-68af-47a7-873c-006c257e840e">PublisherID</a>


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

<a href="https://msdn.microsoft.com/223c57b9-2d70-476b-9f97-0f4d73c36dce">PublisherName</a>


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

<a href="https://msdn.microsoft.com/b92b9493-bfee-4898-9e58-0a1cf9b59ffa">PublisherType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The optional administrative group for the event publisher.

</td>
</tr>
</table> 

