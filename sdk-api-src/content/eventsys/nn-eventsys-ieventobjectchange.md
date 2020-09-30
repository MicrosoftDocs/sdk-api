---
UID: NN:eventsys.IEventObjectChange
title: IEventObjectChange (eventsys.h)
description: Notifies subscribers of changes to the event store.
helpviewer_keywords: ["IEventObjectChange","IEventObjectChange interface [COM+]","IEventObjectChange interface [COM+]","described","_cos_IEventObjectChange","cos.ieventobjectchange","eventsys/IEventObjectChange"]
old-location: cos\ieventobjectchange.htm
tech.root: cos
ms.assetid: 2e916601-e03d-4c5f-a8fb-38317cfb66ad
ms.date: 12/05/2018
ms.keywords: IEventObjectChange, IEventObjectChange interface [COM+], IEventObjectChange interface [COM+],described, _cos_IEventObjectChange, cos.ieventobjectchange, eventsys/IEventObjectChange
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEventObjectChange
 - eventsys/IEventObjectChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Eventsys.h
api_name:
 - IEventObjectChange
---

# IEventObjectChange interface


## -description

Notifies subscribers of changes to the event store.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEventObjectChange</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEventObjectChange</b> also has these types of members:
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
<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventobjectchange-changedeventclass">ChangedEventClass</a>
</td>
<td align="left" width="63%">
Indicates that an event class object has been added, modified, or deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventobjectchange-changedpublisher">ChangedPublisher</a>
</td>
<td align="left" width="63%">
Indicates a publisher object has been added, modified, or deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/eventsys/nf-eventsys-ieventobjectchange-changedsubscription">ChangedSubscription</a>
</td>
<td align="left" width="63%">
Indicates that a subscription object has been added, modified, or deleted.


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/eventsys/nn-eventsys-ieventsystem">IEventSystem</a>