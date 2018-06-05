---
UID: NF:tapi3if.ITQOSEvent.get_Event
title: ITQOSEvent::get_Event
author: windows-sdk-content
description: The get_Event method gets the QOS_EVENT indicator.
old-location: tapi3\itqosevent_get_event.htm
old-project: Tapi
ms.assetid: 8e0f4705-6614-4973-85bd-21abd17bd7fe
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITQOSEvent interface [TAPI 2.2],get_Event method, ITQOSEvent.get_Event, ITQOSEvent::get_Event, _tapi3_itqosevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITQOSEvent interface, tapi3.itqosevent_get_event, tapi3if/ITQOSEvent::get_Event
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITQOSEvent.get_Event
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITQOSEvent::get_Event


## -description


The 
<b>get_Event</b> method gets the 
<a href="https://msdn.microsoft.com/8bf4bfdc-6327-497d-9d19-4771d47982bb">QOS_EVENT</a> indicator.


## -parameters




### -param pQosEvent [out]

Indicator of the QOS event type.


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
The <i>pQosEvent</i> parameter is not a valid pointer.

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




<a href="https://msdn.microsoft.com/6e3a8aef-bd76-4047-9018-801a3cab2c62">ITQOSEvent</a>



<a href="https://msdn.microsoft.com/8bf4bfdc-6327-497d-9d19-4771d47982bb">QOS_EVENT</a>
 

 

