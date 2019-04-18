---
UID: NF:tapi3if.ITCallMediaEvent.get_Cause
title: ITCallMediaEvent::get_Cause (tapi3if.h)
author: windows-sdk-content
description: The get_Cause method gets the cause of the call media event, such as a timeout on the renderer device.
old-location: tapi3\itcallmediaevent_get_cause.htm
tech.root: Tapi
ms.assetid: 51905e69-ff95-46fb-a73a-785a8d444253
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITCallMediaEvent interface [TAPI 2.2],get_Cause method, ITCallMediaEvent.get_Cause, ITCallMediaEvent::get_Cause, _tapi3_itcallmediaevent_get_cause, get_Cause, get_Cause method [TAPI 2.2], get_Cause method [TAPI 2.2],ITCallMediaEvent interface, tapi3.itcallmediaevent_get_cause, tapi3if/ITCallMediaEvent::get_Cause
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
 - ITCallMediaEvent.get_Cause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCallMediaEvent::get_Cause


## -description


The 
<b>get_Cause</b> method gets the cause of the call media event, such as a timeout on the renderer device.


## -parameters




### -param pCause [out]

Pointer to 
<a href="https://msdn.microsoft.com/c43e0a72-decc-47e3-bd5e-d94a95a2e404">CALL_MEDIA_EVENT_CAUSE</a>.


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
The <i>pCause</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c43e0a72-decc-47e3-bd5e-d94a95a2e404">CALL_MEDIA_EVENT_CAUSE</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>
 

 

