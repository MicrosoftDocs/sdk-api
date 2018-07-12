---
UID: NF:tapi3cc.ITAgentSessionEvent.get_Event
title: ITAgentSessionEvent::get_Event
author: windows-sdk-content
description: The get_Event method gets an AGENT_SESSION_EVENT descriptor of the event that occurred.
old-location: tapi3\itagentsessionevent_get_event.htm
old-project: tapi
ms.assetid: 34779590-c2f6-4bd7-932b-5ac6365bcb20
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITAgentSessionEvent interface [TAPI 2.2],get_Event method, ITAgentSessionEvent.get_Event, ITAgentSessionEvent::get_Event, _tapi3_itagentsessionevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITAgentSessionEvent interface, tapi3.itagentsessionevent_get_event, tapi3cc/ITAgentSessionEvent::get_Event
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AGENT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgentSessionEvent.get_Event
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentSessionEvent::get_Event


## -description


The 
<b>get_Event</b> method gets an 
<a href="https://msdn.microsoft.com/44eb7669-6c0b-4b9c-a209-9f15f27a1ba9">AGENT_SESSION_EVENT</a> descriptor of the event that occurred.


## -parameters




### -param pEvent [out]

Pointer to the 
<a href="https://msdn.microsoft.com/44eb7669-6c0b-4b9c-a209-9f15f27a1ba9">AGENT_SESSION_EVENT</a> descriptor of the event.


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




<a href="https://msdn.microsoft.com/44eb7669-6c0b-4b9c-a209-9f15f27a1ba9">AGENT_SESSION_EVENT</a>



<a href="https://msdn.microsoft.com/70d37d06-b1a6-4f7e-bfe5-731d1b4cd66b">ITAgentSessionEvent</a>
 

 

