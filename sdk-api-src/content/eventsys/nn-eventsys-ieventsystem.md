---
UID: NN:eventsys.IEventSystem
title: IEventSystem
author: windows-sdk-content
description: Provides access to the event data store.
old-location: cos\ieventsystem.htm
old-project: cossdk
ms.assetid: 29b3e552-b717-4d10-9fa4-1386da3c5460
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IEventSystem, IEventSystem interface [COM+], IEventSystem interface [COM+],described, _cos_IEventSystem, cos.ieventsystem, eventsys/IEventSystem
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
tech.root: 
req.typenames: EOC_ChangeType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EventSys.h
api_name:
 - IEventSystem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventSystem interface


## -description


Provides access to the event data store.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventSystem</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IEventSystem</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406403">Query</a>
</td>
<td align="left" width="63%">

Retrieves a collection of subscription or event objects from the event data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bb76b7b-c19c-43bd-a2cc-fbe7b98fa7b9">QueryS</a>
</td>
<td align="left" width="63%">

Retrieves a collection of subscription or event objects from the event data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes one or more subscription or event objects from the event data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c3d2972-bfc4-43f2-a131-f3b3010a3c91">RemoveS</a>
</td>
<td align="left" width="63%">
Removes one or more subscription or event objects from the event data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9999ba1-9ae1-4fc0-9613-be31961fb514">Store</a>
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

<a href="https://msdn.microsoft.com/58cd529d-f1e5-4777-9999-3f223d27dc64">EventObjectChangeEventClassID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The CLSID of an event class object that notifies the caller of changes to the event store.

</td>
</tr>
</table> 

