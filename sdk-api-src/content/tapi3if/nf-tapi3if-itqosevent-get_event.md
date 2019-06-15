---
UID: NF:tapi3if.ITQOSEvent.get_Event
title: ITQOSEvent::get_Event (tapi3if.h)
author: windows-sdk-content
description: The get_Event method gets the QOS_EVENT indicator.
old-location: tapi3\itqosevent_get_event.htm
tech.root: Tapi
ms.assetid: 8e0f4705-6614-4973-85bd-21abd17bd7fe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITQOSEvent interface [TAPI 2.2],get_Event method, ITQOSEvent.get_Event, ITQOSEvent::get_Event, _tapi3_itqosevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITQOSEvent interface, tapi3.itqosevent_get_event, tapi3if/ITQOSEvent::get_Event
ms.topic: method
f1_keywords: ["tapi3if/ITQOSEvent.get_Event"]
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
 - ITQOSEvent.get_Event
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITQOSEvent::get_Event


## -description


The 
<b>get_Event</b> method gets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-qos_event">QOS_EVENT</a> indicator.


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




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent">ITQOSEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-qos_event">QOS_EVENT</a>
 

 

