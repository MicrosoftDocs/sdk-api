---
UID: NF:tapi3if.ITCallNotificationEvent.get_Event
title: ITCallNotificationEvent::get_Event
author: windows-sdk-content
description: The get_Event method returns a CALL_NOTIFICATION_EVENT description of whether the application owns or is monitoring the call on which the event has occurred.
old-location: tapi3\itcallnotificationevent_get_event.htm
tech.root: tapi
ms.assetid: 08a3925c-e14e-442e-952e-483fc41d049c
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITCallNotificationEvent interface [TAPI 2.2],get_Event method, ITCallNotificationEvent.get_Event, ITCallNotificationEvent::get_Event, _tapi3_itcallnotificationevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITCallNotificationEvent interface, tapi3.itcallnotificationevent_get_event, tapi3if/ITCallNotificationEvent::get_Event
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
 - ITCallNotificationEvent.get_Event
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallNotificationEvent::get_Event


## -description


The 
<b>get_Event</b> method returns a 
<a href="https://msdn.microsoft.com/0c05042f-af1e-4657-bb1c-e6741361b11c">CALL_NOTIFICATION_EVENT</a> description of whether the application owns or is monitoring the call on which the event has occurred.


## -parameters




### -param pCallNotificationEvent [out]

Pointer to the 
<a href="https://msdn.microsoft.com/0c05042f-af1e-4657-bb1c-e6741361b11c">CALL_NOTIFICATION_EVENT</a> description of the application's privilege on the call returned by 
<a href="https://msdn.microsoft.com/6ff82bd1-de69-4ab7-9152-a578b8566755">ITCallNotificationEvent::get_Call</a>.


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
The <i>pCallNotificationEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0c05042f-af1e-4657-bb1c-e6741361b11c">CALL_NOTIFICATION_EVENT</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a>
 

 

