---
UID: NN:eventsys.IEnumEventObject
title: IEnumEventObject (eventsys.h)
description: Enumerates the event objects that are registered in the COM+ events store.
helpviewer_keywords: ["IEnumEventObject","IEnumEventObject interface [COM+]","IEnumEventObject interface [COM+]","described","_cos_ienumeventobject","cos.ienumeventobject","eventsys/IEnumEventObject"]
old-location: cos\ienumeventobject.htm
tech.root: cos
ms.assetid: a42d0791-28d0-4d83-b94d-ff2f8ef9a614
ms.date: 12/05/2018
ms.keywords: IEnumEventObject, IEnumEventObject interface [COM+], IEnumEventObject interface [COM+],described, _cos_ienumeventobject, cos.ienumeventobject, eventsys/IEnumEventObject
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
 - IEnumEventObject
 - eventsys/IEnumEventObject
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
 - IEnumEventObject
---

# IEnumEventObject interface


## -description

Enumerates the event objects that are registered in the COM+ events store.

Similar functionality is available through <a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventobjectcollection">IEventObjectCollection</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumEventObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumEventObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumEventObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ienumeventobject-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates an enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ienumeventobject-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ienumeventobject-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nf-eventsys-ienumeventobject-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/eventsys/nn-eventsys-ieventobjectcollection">IEventObjectCollection</a>

