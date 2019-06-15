---
UID: NN:eventsys.IEventObjectCollection
title: IEventObjectCollection (eventsys.h)
author: windows-sdk-content
description: Manages objects in an event objects collection.
old-location: cos\ieventobjectcollection.htm
tech.root: cossdk
ms.assetid: 7bb00b80-a48f-49c8-983d-9ff0ea424e4d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEventObjectCollection, IEventObjectCollection interface [COM+], IEventObjectCollection interface [COM+],described, _cos_IEventObjectCollection, cos.ieventobjectcollection, eventsys/IEventObjectCollection
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
 - IEventObjectCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventObjectCollection interface


## -description


Manages objects in an event objects collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventObjectCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEventObjectCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IEventObjectCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventobjectcollection-add">Add</a>
</td>
<td align="left" width="63%">
Adds an event object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventobjectcollection-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an event object from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventObjectCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventobjectcollection-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An enumerator for the objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventobjectcollection-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventobjectcollection-get_item">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An item in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventobjectcollection-get_newenum">NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An enumeration object that implements <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ienumeventobject">IEnumEventObject</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ienumeventobject">IEnumEventObject</a>
 

 

