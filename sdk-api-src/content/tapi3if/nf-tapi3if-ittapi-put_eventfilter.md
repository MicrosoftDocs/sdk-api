---
UID: NF:tapi3if.ITTAPI.put_EventFilter
title: ITTAPI::put_EventFilter
author: windows-sdk-content
description: The put_EventFilter method sets the event filter mask. The mask is a series of ORed members of the TAPI_EVENT enumeration.
old-location: tapi3\ittapi_put_eventfilter.htm
tech.root: tapi
ms.assetid: 126ec551-aade-47d8-987f-1f735f10bd28
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITTAPI interface [TAPI 2.2],put_EventFilter method, ITTAPI.put_EventFilter, ITTAPI::put_EventFilter, _tapi3_ittapi_put_eventfilter, put_EventFilter, put_EventFilter method [TAPI 2.2], put_EventFilter method [TAPI 2.2],ITTAPI interface, tapi3.ittapi_put_eventfilter, tapi3if/ITTAPI::put_EventFilter
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
 - ITTAPI.put_EventFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPI::put_EventFilter


## -description


The 
<b>put_EventFilter</b> method sets the event filter mask. The mask is a series of ORed members of the 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> enumeration.
<div class="alert"><b>Note</b>  You must call this method to enable reception of events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events.</div><div> </div>

## -parameters




### -param lFilterMask [in]

Event filter mask.


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



<a href="https://msdn.microsoft.com/c0544e9f-0bfc-43ab-bcf0-800afb0ebfcf">get_EventFilter</a>
 

 

