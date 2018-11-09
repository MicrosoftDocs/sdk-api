---
UID: NF:tapi3cc.ITQueueEvent.get_Event
title: ITQueueEvent::get_Event
author: windows-sdk-content
description: The get_Event method gets the descriptor of the event that occurred.
old-location: tapi3\itqueueevent_get_event.htm
tech.root: tapi
ms.assetid: 704a9601-e8c3-42d4-86bc-be59c44a05b3
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITQueueEvent interface [TAPI 2.2],get_Event method, ITQueueEvent.get_Event, ITQueueEvent::get_Event, _tapi3_itqueueevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITQueueEvent interface, tapi3.itqueueevent_get_event, tapi3cc/ITQueueEvent::get_Event
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITQueueEvent.get_Event
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITQueueEvent::get_Event


## -description


The 
<b>get_Event</b> method gets the descriptor of the event that occurred.


## -parameters




### -param pEvent [out]

Pointer to 
<a href="https://msdn.microsoft.com/5a2efb70-a943-46c5-a362-18579ad8c965">ACDQUEUE_EVENT</a> descriptor of event.


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




<a href="https://msdn.microsoft.com/5a2efb70-a943-46c5-a362-18579ad8c965">ACDQUEUE_EVENT</a>



<a href="https://msdn.microsoft.com/7e4655ff-6ed4-4166-91f7-49d2e0556662">ITQueueEvent</a>
 

 

