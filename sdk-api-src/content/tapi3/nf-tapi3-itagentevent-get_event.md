---
UID: NF:tapi3.ITAgentEvent.get_Event
title: ITAgentEvent::get_Event
author: windows-sdk-content
description: Gets an AGENT_EVENT descriptor of the event that occurred.
old-location: tapi3\itagentevent_get_event.htm
old-project: tapi
ms.assetid: d402b2b4-2817-4ebe-b735-69ea9e975f54
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITAgentEvent interface [TAPI 2.2],get_Event method, ITAgentEvent.get_Event, ITAgentEvent::get_Event, _tapi3_itagentevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITAgentEvent interface, tapi3.itagentevent_get_event, tapi3cc/ITAgentEvent::get_Event
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3.h
req.include-header: Tapi3.h
req.redist: 
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
req.typenames: MSP_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgentEvent.get_Event
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentEvent::get_Event


## -description


Gets an 
<a href="https://msdn.microsoft.com/9dec832a-98da-436a-89c8-d5c69053082a">AGENT_EVENT</a> descriptor of the event that occurred.


## -parameters




### -param pEvent [out]

Pointer to 
<a href="https://msdn.microsoft.com/9dec832a-98da-436a-89c8-d5c69053082a">AGENT_EVENT</a> descriptor of event.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9dec832a-98da-436a-89c8-d5c69053082a">AGENT_EVENT</a>



<a href="https://msdn.microsoft.com/adfb58f7-b02c-4a64-92c1-a1b29c9f7143">ITAgentEvent</a>
 

 

