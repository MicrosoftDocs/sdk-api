---
UID: NF:tapi3if.ITTAPI.get_EventFilter
title: ITTAPI::get_EventFilter
author: windows-sdk-content
description: The get_EventFilter method gets the current event filter mask. The mask is a series of ORed members of the TAPI_EVENT enumeration.
old-location: tapi3\ittapi_get_eventfilter.htm
tech.root: tapi
ms.assetid: c0544e9f-0bfc-43ab-bcf0-800afb0ebfcf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITTAPI interface [TAPI 2.2],get_EventFilter method, ITTAPI.get_EventFilter, ITTAPI::get_EventFilter, _tapi3_ittapi_get_eventfilter, get_EventFilter, get_EventFilter method [TAPI 2.2], get_EventFilter method [TAPI 2.2],ITTAPI interface, tapi3.ittapi_get_eventfilter, tapi3if/ITTAPI::get_EventFilter
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
 - ITTAPI.get_EventFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPI::get_EventFilter


## -description


The 
<b>get_EventFilter</b> method gets the current event filter mask. The mask is a series of ORed members of the 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> enumeration.


## -parameters




### -param plFilterMask [out]

Pointer to the event filter mask.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events overview</a>



<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a>



<a href="https://msdn.microsoft.com/06cfe56c-907f-49ed-8a7a-db31383a06f9">ITTAPIEventNotification</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>



<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">put_EventFilter</a>
 

 

