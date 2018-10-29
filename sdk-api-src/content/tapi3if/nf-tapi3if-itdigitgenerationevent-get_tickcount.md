---
UID: NF:tapi3if.ITDigitGenerationEvent.get_TickCount
title: ITDigitGenerationEvent::get_TickCount
author: windows-sdk-content
description: The get_TickCount method gets the &#0034;tick count&#0034; (number of milliseconds since Windows started) at which the digit generation completed.
old-location: tapi3\itdigitgenerationevent_get_tickcount.htm
tech.root: Tapi
ms.assetid: daae0ae5-0eaf-4ca7-b08a-1c46b9ebfcab
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITDigitGenerationEvent interface [TAPI 2.2],get_TickCount method, ITDigitGenerationEvent.get_TickCount, ITDigitGenerationEvent::get_TickCount, _tapi3_itdigitgenerationevent_get_tickcount, get_TickCount, get_TickCount method [TAPI 2.2], get_TickCount method [TAPI 2.2],ITDigitGenerationEvent interface, tapi3.itdigitgenerationevent_get_tickcount, tapi3if/ITDigitGenerationEvent::get_TickCount
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
 - ITDigitGenerationEvent.get_TickCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDigitGenerationEvent::get_TickCount


## -description


The 
<b>get_TickCount</b> method gets the "tick count" (number of milliseconds since Windows started) at which the digit generation completed.


## -parameters




### -param plTickCount [out]

Pointer to tick count.


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
The <i>plTickCount</i> parameter is not a valid pointer.

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




<a href="https://msdn.microsoft.com/788eee9c-b885-4b94-b259-694353c0f63a">ITDigitGenerationEvent</a>
 

 

