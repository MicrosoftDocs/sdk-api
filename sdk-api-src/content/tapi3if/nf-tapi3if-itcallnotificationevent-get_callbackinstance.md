---
UID: NF:tapi3if.ITCallNotificationEvent.get_CallbackInstance
title: ITCallNotificationEvent::get_CallbackInstance
author: windows-sdk-content
description: The get_CallbackInstance method gets a pointer to the callback instance associated with this event.
old-location: tapi3\itcallnotificationevent_get_callbackinstance.htm
tech.root: tapi
ms.assetid: daa6d980-49aa-4e5a-9871-77e39dcdb6f0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITCallNotificationEvent interface [TAPI 2.2],get_CallbackInstance method, ITCallNotificationEvent.get_CallbackInstance, ITCallNotificationEvent::get_CallbackInstance, _tapi3_itcallnotificationevent_get_callbackinstance, get_CallbackInstance, get_CallbackInstance method [TAPI 2.2], get_CallbackInstance method [TAPI 2.2],ITCallNotificationEvent interface, tapi3.itcallnotificationevent_get_callbackinstance, tapi3if/ITCallNotificationEvent::get_CallbackInstance
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
 - ITCallNotificationEvent.get_CallbackInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallNotificationEvent::get_CallbackInstance


## -description


The 
<b>get_CallbackInstance</b> method gets a pointer to the callback instance associated with this event.


## -parameters




### -param plCallbackInstance [out]

Pointer to callback instance returned by 
<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>.


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
The <i>plCallbackInstance</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a>



<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>
 

 

