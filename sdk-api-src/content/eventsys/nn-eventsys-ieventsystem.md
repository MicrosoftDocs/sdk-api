---
UID: NN:eventsys.IEventSystem
title: IEventSystem (eventsys.h)
description: Provides access to the event data store.
helpviewer_keywords: ["IEventSystem","IEventSystem interface [COM+]","IEventSystem interface [COM+]","described","_cos_IEventSystem","cos.ieventsystem","eventsys/IEventSystem"]
old-location: cos\ieventsystem.htm
tech.root: cos
ms.assetid: 29b3e552-b717-4d10-9fa4-1386da3c5460
ms.date: 12/05/2018
ms.keywords: IEventSystem, IEventSystem interface [COM+], IEventSystem interface [COM+],described, _cos_IEventSystem, cos.ieventsystem, eventsys/IEventSystem
f1_keywords:
- eventsys/IEventSystem
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
- IEventSystem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventSystem interface


## -description


Provides access to the event data store.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventSystem</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEventSystem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IEventSystem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsystem-query">Query</a>
</td>
<td align="left" width="63%">
Retrieves a collection of subscription or event objects from the event data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsystem-querys">QueryS</a>
</td>
<td align="left" width="63%">
Retrieves a collection of subscription or event objects from the event data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsystem-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes one or more subscription or event objects from the event data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsystem-removes">RemoveS</a>
</td>
<td align="left" width="63%">
Removes one or more subscription or event objects from the event data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsystem-store">Store</a>
</td>
<td align="left" width="63%">
Creates or modifies an event or subscription object within the event system.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventSystem</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventsystem-get_eventobjectchangeeventclassid">EventObjectChangeEventClassID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The CLSID of an event class object that notifies the caller of changes to the event store.

</td>
</tr>
</table> 

