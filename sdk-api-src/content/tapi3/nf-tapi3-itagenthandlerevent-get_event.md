---
UID: NF:tapi3.ITAgentHandlerEvent.get_Event
title: ITAgentHandlerEvent::get_Event
author: windows-sdk-content
description: The get_Event method gets the description for the event that has occurred.
old-location: tapi3\itagenthandlerevent_get_event.htm
tech.root: Tapi
ms.assetid: 3362964c-15d3-497c-876b-46e8d26389c0
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITAgentHandlerEvent interface [TAPI 2.2],get_Event method, ITAgentHandlerEvent.get_Event, ITAgentHandlerEvent::get_Event, _tapi3_itagenthandlerevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITAgentHandlerEvent interface, tapi3.itagenthandlerevent_get_event, tapi3cc/ITAgentHandlerEvent::get_Event
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
 - ITAgentHandlerEvent.get_Event
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAgentHandlerEvent::get_Event


## -description


The 
<b>get_Event</b> method gets the description for the event that has occurred.


## -parameters




### -param pEvent [out]

Pointer to the 
<a href="https://msdn.microsoft.com/6d8340a9-dfe5-43bc-a223-d534f5b90cba">AGENTHANDLER_EVENT</a> descriptor.


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




<a href="https://msdn.microsoft.com/6d8340a9-dfe5-43bc-a223-d534f5b90cba">AGENTHANDLER_EVENT</a>



<a href="https://msdn.microsoft.com/c61becce-09fd-4b12-bbc9-98df57d5f0d3">ITAgentHandlerEvent</a>
 

 

