---
UID: NF:tapi3if.ITDigitDetectionEvent.get_Call
title: ITDigitDetectionEvent::get_Call
author: windows-sdk-content
description: The get_Call method gets a pointer to the ITCallInfo interface for the call on which the event occurred.
old-location: tapi3\itdigitdetectionevent_get_call.htm
tech.root: tapi
ms.assetid: 98168b0c-132b-47cf-9d5d-6fba7b570216
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITDigitDetectionEvent interface [TAPI 2.2],get_Call method, ITDigitDetectionEvent.get_Call, ITDigitDetectionEvent::get_Call, _tapi3_itdigitdetectionevent_get_call, get_Call, get_Call method [TAPI 2.2], get_Call method [TAPI 2.2],ITDigitDetectionEvent interface, tapi3.itdigitdetectionevent_get_call, tapi3if/ITDigitDetectionEvent::get_Call
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
 - ITDigitDetectionEvent.get_Call
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDigitDetectionEvent::get_Call


## -description


The 
<b>get_Call</b> method gets a pointer to the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface for the call on which the event occurred.


## -parameters




### -param ppCallInfo [out]

Pointer to 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface.


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
The <i>ppCallInfo</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f387f5f5-06e4-45f2-8d93-31ff0da6151a">ITDigitDetectionEvent</a>
 

 

