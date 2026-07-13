---
UID: NF:tapi3cc.ITQueueEvent.get_Event
title: ITQueueEvent::get_Event (tapi3cc.h)
description: The ITQueueEvent::get_Event method (tapi3cc.h) gets the descriptor of the event that occurred.
helpviewer_keywords: ["ITQueueEvent interface [TAPI 2.2]","get_Event method","ITQueueEvent.get_Event","ITQueueEvent::get_Event","_tapi3_itqueueevent_get_event","get_Event","get_Event method [TAPI 2.2]","get_Event method [TAPI 2.2]","ITQueueEvent interface","tapi3.itqueueevent_get_event","tapi3cc/ITQueueEvent::get_Event"]
old-location: tapi3\itqueueevent_get_event.htm
tech.root: tapi3
ms.assetid: 704a9601-e8c3-42d4-86bc-be59c44a05b3
ms.date: 08/10/2022
ms.keywords: ITQueueEvent interface [TAPI 2.2],get_Event method, ITQueueEvent.get_Event, ITQueueEvent::get_Event, _tapi3_itqueueevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITQueueEvent interface, tapi3.itqueueevent_get_event, tapi3cc/ITQueueEvent::get_Event
req.header: tapi3cc.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITQueueEvent::get_Event
 - tapi3cc/ITQueueEvent::get_Event
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITQueueEvent.get_Event
---

# ITQueueEvent::get_Event


## -description

The 
<b>get_Event</b> method gets the descriptor of the event that occurred.

## -parameters

### -param pEvent [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/ne-tapi3-acdqueue_event">ACDQUEUE_EVENT</a> descriptor of event.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pEvent</i> is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3/ne-tapi3-acdqueue_event">ACDQUEUE_EVENT</a>



<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueueevent">ITQueueEvent</a>
