---
UID: NF:tapi3if.ITDigitGenerationEvent.get_CallbackInstance
title: ITDigitGenerationEvent::get_CallbackInstance
author: windows-sdk-content
description: The get_CallbackInstance method gets a pointer to the callback instance associated with the event.
old-location: tapi3\itdigitgenerationevent_get_callbackinstance.htm
tech.root: tapi
ms.assetid: e0cc1e75-bdc2-4b05-a83b-13e4778ed75b
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITDigitGenerationEvent interface [TAPI 2.2],get_CallbackInstance method, ITDigitGenerationEvent.get_CallbackInstance, ITDigitGenerationEvent::get_CallbackInstance, _tapi3_itdigitgenerationevent_get_callbackinstance, get_CallbackInstance, get_CallbackInstance method [TAPI 2.2], get_CallbackInstance method [TAPI 2.2],ITDigitGenerationEvent interface, tapi3.itdigitgenerationevent_get_callbackinstance, tapi3if/ITDigitGenerationEvent::get_CallbackInstance
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
 - ITDigitGenerationEvent.get_CallbackInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDigitGenerationEvent::get_CallbackInstance


## -description


The 
<b>get_CallbackInstance</b> method gets a pointer to the callback instance associated with the event.


## -parameters




### -param plCallbackInstance [out]

Pointer to the callback instance returned by 
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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plCallbackInstance</i> parameter is not a valid pointer.

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




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/788eee9c-b885-4b94-b259-694353c0f63a">ITDigitGenerationEvent</a>



<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>
 

 

