---
UID: NF:tapi3if.ITToneDetectionEvent.get_CallbackInstance
title: ITToneDetectionEvent::get_CallbackInstance
author: windows-sdk-content
description: The get_CallbackInstance method gets a pointer to the application's callback function that will process the event.
old-location: tapi3\ittonedetectionevent_get_callbackinstance.htm
old-project: Tapi
ms.assetid: 5ebd7fae-0060-4937-9812-8b48eceb9139
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITToneDetectionEvent interface [TAPI 2.2],get_CallbackInstance method, ITToneDetectionEvent.get_CallbackInstance, ITToneDetectionEvent::get_CallbackInstance, _tapi3_ittonedetectionevent_get_callbackinstance, get_CallbackInstance, get_CallbackInstance method [TAPI 2.2], get_CallbackInstance method [TAPI 2.2],ITToneDetectionEvent interface, tapi3.ittonedetectionevent_get_callbackinstance, tapi3if/ITToneDetectionEvent::get_CallbackInstance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: 
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITToneDetectionEvent.get_CallbackInstance
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITToneDetectionEvent::get_CallbackInstance


## -description


The 
<b>get_CallbackInstance</b> method gets a pointer to the application's callback function that will process the event.


## -parameters




### -param plCallbackInstance [out]

Pointer to the callback instance returned by the 
<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a> method.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code/value</th>
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
<dt>8</dt>
</dl>
</td>
<td width="60%">
LegacyMediaControl2 Enums

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">ITTAPI::RegisterCallNotifications</a>



<a href="https://msdn.microsoft.com/1e0f71a2-1aae-46b7-9147-7bf9da4d9503">ITToneDetectionEvent</a>
 

 

