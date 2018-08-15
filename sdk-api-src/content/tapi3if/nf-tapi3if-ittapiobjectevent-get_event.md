---
UID: NF:tapi3if.ITTAPIObjectEvent.get_Event
title: ITTAPIObjectEvent::get_Event
author: windows-sdk-content
description: The get_Event method gets information concerning an asynchronous event notification. The application uses TAPIOBJECT_EVENT to determine what type of event is being signaled.
old-location: tapi3\ittapiobjectevent_get_event.htm
old-project: tapi
ms.assetid: 5ae4362f-6987-461e-928f-9478e37e0380
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITTAPIObjectEvent interface [TAPI 2.2],get_Event method, ITTAPIObjectEvent.get_Event, ITTAPIObjectEvent::get_Event, _tapi3_ittapiobjectevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITTAPIObjectEvent interface, tapi3.ittapiobjectevent_get_event, tapi3if/ITTAPIObjectEvent::get_Event
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTAPIObjectEvent.get_Event
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTAPIObjectEvent::get_Event


## -description


The 
<b>get_Event</b> method gets information concerning an asynchronous event notification. The application uses 
<a href="https://msdn.microsoft.com/606e9f99-d90c-4d4a-8dd5-2734c9bd2e7e">TAPIOBJECT_EVENT</a> to determine what type of event is being signaled.


## -parameters




### -param pEvent [out]


<a href="https://msdn.microsoft.com/606e9f99-d90c-4d4a-8dd5-2734c9bd2e7e">TAPIOBJECT_EVENT</a> indicator of the event.


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
The <i>pEvent</i> parameter is not a valid pointer.

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




<a href="https://msdn.microsoft.com/73be7109-0d3a-4ac5-adb7-e1577d8640b5">ITTAPIObjectEvent</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>



<a href="https://msdn.microsoft.com/606e9f99-d90c-4d4a-8dd5-2734c9bd2e7e">TAPIOBJECT_EVENT</a>
 

 

