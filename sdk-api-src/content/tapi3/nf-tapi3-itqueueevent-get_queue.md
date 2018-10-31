---
UID: NF:tapi3.ITQueueEvent.get_Queue
title: ITQueueEvent::get_Queue
author: windows-sdk-content
description: The get_Queue method gets a pointer to the queue on which the event occurred.
old-location: tapi3\itqueueevent_get_queue.htm
tech.root: tapi
ms.assetid: 59a4be82-0118-4a9c-9f85-0febfe1b3e18
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITQueueEvent interface [TAPI 2.2],get_Queue method, ITQueueEvent.get_Queue, ITQueueEvent::get_Queue, _tapi3_itqueueevent_get_queue, get_Queue, get_Queue method [TAPI 2.2], get_Queue method [TAPI 2.2],ITQueueEvent interface, tapi3.itqueueevent_get_queue, tapi3cc/ITQueueEvent::get_Queue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3.h
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
 - ITQueueEvent.get_Queue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITQueueEvent::get_Queue


## -description


The 
<b>get_Queue</b> method gets a pointer to the queue on which the event occurred.


## -parameters




### -param ppQueue [out]

Pointer to 
<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a> interface on which event occurred.


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
<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a> interface returned by <b>ITQueueEvent::get_Queue</b>. The application must call <b>Release</b> on the 
<b>ITQueue</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/dd1bc6c7-4d4e-4f66-ac5a-7004b85ec023">ITQueue</a>



<a href="https://msdn.microsoft.com/7e4655ff-6ed4-4166-91f7-49d2e0556662">ITQueueEvent</a>
 

 

