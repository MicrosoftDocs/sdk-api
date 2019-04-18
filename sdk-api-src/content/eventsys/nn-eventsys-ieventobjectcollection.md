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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventObjectCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IEventObjectCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ca08e56a-2ade-4209-a61a-b9dae021e888">Add</a>
</td>
<td align="left" width="63%">
Adds an event object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5092b1e1-bbf2-493c-92be-41196b43d4f2">Remove</a>
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

<a href="https://msdn.microsoft.com/bdf2bcb0-42c2-4904-b36b-73ee27f4c188">_NewEnum</a>


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

<a href="https://msdn.microsoft.com/eb4558e3-60bb-4fcb-b998-b812e76bd8d0">Count</a>


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

<a href="https://msdn.microsoft.com/6d037759-3b13-4f4d-b27d-a3a20be0f0aa">Item</a>


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

<a href="https://msdn.microsoft.com/5e4e0749-bf23-4174-af80-0b708dbaf432">NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An enumeration object that implements <a href="https://msdn.microsoft.com/a42d0791-28d0-4d83-b94d-ff2f8ef9a614">IEnumEventObject</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a42d0791-28d0-4d83-b94d-ff2f8ef9a614">IEnumEventObject</a>
 

 

