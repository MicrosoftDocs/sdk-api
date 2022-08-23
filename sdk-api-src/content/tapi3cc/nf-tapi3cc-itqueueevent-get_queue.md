---
UID: NF:tapi3cc.ITQueueEvent.get_Queue
title: ITQueueEvent::get_Queue (tapi3cc.h)
description: The ITQueueEvent::get_Queue method (tapi3cc.h) gets a pointer to the queue on which the event occurred.
helpviewer_keywords: ["ITQueueEvent interface [TAPI 2.2]","get_Queue method","ITQueueEvent.get_Queue","ITQueueEvent::get_Queue","_tapi3_itqueueevent_get_queue","get_Queue","get_Queue method [TAPI 2.2]","get_Queue method [TAPI 2.2]","ITQueueEvent interface","tapi3.itqueueevent_get_queue","tapi3cc/ITQueueEvent::get_Queue"]
old-location: tapi3\itqueueevent_get_queue.htm
tech.root: tapi3
ms.assetid: 59a4be82-0118-4a9c-9f85-0febfe1b3e18
ms.date: 08/10/2022
ms.keywords: ITQueueEvent interface [TAPI 2.2],get_Queue method, ITQueueEvent.get_Queue, ITQueueEvent::get_Queue, _tapi3_itqueueevent_get_queue, get_Queue, get_Queue method [TAPI 2.2], get_Queue method [TAPI 2.2],ITQueueEvent interface, tapi3.itqueueevent_get_queue, tapi3cc/ITQueueEvent::get_Queue
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
 - ITQueueEvent::get_Queue
 - tapi3cc/ITQueueEvent::get_Queue
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
 - ITQueueEvent.get_Queue
---

# ITQueueEvent::get_Queue


## -description

The 
<b>get_Queue</b> method gets a pointer to the queue on which the event occurred.

## -parameters

### -param ppQueue [out]

Pointer to 
<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueue">ITQueue</a> interface on which event occurred.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The <i>ppQueue</i> is not a valid pointer.

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

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueue">ITQueue</a> interface returned by <b>ITQueueEvent::get_Queue</b>. The application must call <b>Release</b> on the 
<b>ITQueue</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueue">ITQueue</a>



<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueueevent">ITQueueEvent</a>
