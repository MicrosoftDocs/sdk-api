---
UID: NF:tapi3if.ITCallInfoChangeEvent.get_CallbackInstance
title: ITCallInfoChangeEvent::get_CallbackInstance
author: windows-sdk-content
description: The get_CallbackInstance method gets a pointer to the callback instance associated with this event.
old-location: tapi3\itcallinfochangeevent_get_callbackinstance.htm
tech.root: Tapi
ms.assetid: feb9fbcd-58e6-48c7-ab21-9ba0fd766b25
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITCallInfoChangeEvent interface [TAPI 2.2],get_CallbackInstance method, ITCallInfoChangeEvent.get_CallbackInstance, ITCallInfoChangeEvent::get_CallbackInstance, _tapi3_itcallinfochangeevent_get_callbackinstance, get_CallbackInstance, get_CallbackInstance method [TAPI 2.2], get_CallbackInstance method [TAPI 2.2],ITCallInfoChangeEvent interface, tapi3.itcallinfochangeevent_get_callbackinstance, tapi3if/ITCallInfoChangeEvent::get_CallbackInstance
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
 - ITCallInfoChangeEvent.get_CallbackInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallInfoChangeEvent::get_CallbackInstance


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



<a href="https://msdn.microsoft.com/f543da95-c0cc-4631-b91e-ba02dde2c081">ITCallInfoChangeEvent</a>



<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>
 

 

