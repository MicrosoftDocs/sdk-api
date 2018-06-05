---
UID: NN:eventsys.IEventObjectChange
title: IEventObjectChange
author: windows-sdk-content
description: Notifies subscribers of changes to the event store.
old-location: cos\ieventobjectchange.htm
old-project: cossdk
ms.assetid: 2e916601-e03d-4c5f-a8fb-38317cfb66ad
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IEventObjectChange, IEventObjectChange interface [COM+], IEventObjectChange interface [COM+],described, _cos_IEventObjectChange, cos.ieventobjectchange, eventsys/IEventObjectChange
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
tech.root: 
req.typenames: EOC_ChangeType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Eventsys.h
api_name:
-	IEventObjectChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEventObjectChange interface


## -description


Notifies subscribers of changes to the event store.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventObjectChange</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEventObjectChange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEventObjectChange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8db711c8-7c01-4fb0-975c-a66c83063124">ChangedEventClass</a>
</td>
<td align="left" width="63%">

Indicates that an event class object has been added, modified, or deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13bd95e6-5fc2-41e2-9002-67a87f727528">ChangedPublisher</a>
</td>
<td align="left" width="63%">

Indicates a publisher object has been added, modified, or deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61d67705-b225-4f9e-98a5-cb636989f44f">ChangedSubscription</a>
</td>
<td align="left" width="63%">
Indicates that a subscription object has been added, modified, or deleted.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/29b3e552-b717-4d10-9fa4-1386da3c5460">IEventSystem</a>
 

 

