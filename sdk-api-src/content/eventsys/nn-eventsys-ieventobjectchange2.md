---
UID: NN:eventsys.IEventObjectChange2
title: IEventObjectChange2 (eventsys.h)
description: Notifies subscribers of changes to the event store while including partition and application ID information.
old-location: cos\ieventobjectchange2.htm
tech.root: cossdk
ms.assetid: 1b51c7ad-eae7-4030-81c2-ed9259648d31
ms.date: 12/05/2018
ms.keywords: IEventObjectChange2, IEventObjectChange2 interface [COM+], IEventObjectChange2 interface [COM+],described, _cos_IEventObjectChange2, cos.ieventobjectchange2, eventsys/IEventObjectChange2
ms.topic: interface
f1_keywords:
- eventsys/IEventObjectChange2
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
- IEventObjectChange2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEventObjectChange2 interface


## -description


Notifies subscribers of changes to the event store while including partition and application ID information.

The <b>IEventObjectChange2</b> interface has the same firing characteristics as <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventobjectchange">IEventObjectChange</a>. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventObjectChange2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEventObjectChange2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEventObjectChange2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventobjectchange2-changedeventclass">ChangedEventClass</a>
</td>
<td align="left" width="63%">
Indicates that an event class object has been added, modified, or deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ieventobjectchange2-changedsubscription">ChangedSubscription</a>
</td>
<td align="left" width="63%">
Indicates that a subscription object has been added, modified, or deleted.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventobjectchange">IEventObjectChange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventsystem">IEventSystem</a>
 

 

