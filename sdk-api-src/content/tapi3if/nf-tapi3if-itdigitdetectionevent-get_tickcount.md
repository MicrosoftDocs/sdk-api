---
UID: NF:tapi3if.ITDigitDetectionEvent.get_TickCount
title: ITDigitDetectionEvent::get_TickCount
author: windows-driver-content
description: The get_TickCount method gets the &#0034;tick count&#0034; (number of milliseconds since Windows started) at which the digit gathering completed.
old-location: tapi3\itdigitdetectionevent_get_tickcount.htm
old-project: Tapi
ms.assetid: 24c83763-366b-4e1b-8662-9d87250b7945
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: ITDigitDetectionEvent interface [TAPI 2.2],get_TickCount method, ITDigitDetectionEvent.get_TickCount, ITDigitDetectionEvent::get_TickCount, _tapi3_itdigitdetectionevent_get_tickcount, get_TickCount, get_TickCount method [TAPI 2.2], get_TickCount method [TAPI 2.2],ITDigitDetectionEvent interface, tapi3.itdigitdetectionevent_get_tickcount, tapi3if/ITDigitDetectionEvent::get_TickCount
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITDigitDetectionEvent.get_TickCount
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITDigitDetectionEvent::get_TickCount


## -description


The 
<b>get_TickCount</b> method gets the "tick count" (number of milliseconds since Windows started) at which the digit gathering completed.


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
The <i>plTickCount</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f387f5f5-06e4-45f2-8d93-31ff0da6151a">ITDigitDetectionEvent</a>
 

 

