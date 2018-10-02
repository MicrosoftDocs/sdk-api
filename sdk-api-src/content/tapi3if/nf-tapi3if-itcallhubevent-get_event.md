---
UID: NF:tapi3if.ITCallHubEvent.get_Event
title: ITCallHubEvent::get_Event
author: windows-sdk-content
description: The get_Event method returns a pointer to a CALLHUB_EVENT enum description of the event that occurred.
old-location: tapi3\itcallhubevent_get_event.htm
tech.root: TAPI
ms.assetid: a2515583-e564-413d-b93f-6f2dd7776d7b
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITCallHubEvent interface [TAPI 2.2],get_Event method, ITCallHubEvent.get_Event, ITCallHubEvent::get_Event, _tapi3_itcallhubevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITCallHubEvent interface, tapi3.itcallhubevent_get_event, tapi3if/ITCallHubEvent::get_Event
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITCallHubEvent.get_Event
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallHubEvent::get_Event


## -description


The 
<b>get_Event</b> method returns a pointer to a 
<a href="https://msdn.microsoft.com/199e6c8b-805c-40c6-80d0-2e5803ec85a1">CALLHUB_EVENT</a> enum description of the event that occurred.


## -parameters




### -param pEvent [out]

Pointer to a 
<a href="https://msdn.microsoft.com/199e6c8b-805c-40c6-80d0-2e5803ec85a1">CALLHUB_EVENT</a> enum description of the event.


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




<a href="https://msdn.microsoft.com/199e6c8b-805c-40c6-80d0-2e5803ec85a1">CALLHUB_EVENT</a>



<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub Object</a>



<a href="https://msdn.microsoft.com/4008fc7e-f095-442d-9214-61bfead8cf04">ITCallHubEvent</a>
 

 

