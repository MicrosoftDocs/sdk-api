---
UID: NF:tapi3if.ITDigitDetectionEvent.get_Digit
title: ITDigitDetectionEvent::get_Digit (tapi3if.h)
author: windows-sdk-content
description: The get_Digit method retrieves an unsigned char pointer to the digit that was detected.
old-location: tapi3\itdigitdetectionevent_get_digit.htm
tech.root: Tapi
ms.assetid: b62418de-9a3e-46f1-88d9-7e147859ec96
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITDigitDetectionEvent interface [TAPI 2.2],get_Digit method, ITDigitDetectionEvent.get_Digit, ITDigitDetectionEvent::get_Digit, _tapi3_itdigitdetectionevent_get_digit, get_Digit, get_Digit method [TAPI 2.2], get_Digit method [TAPI 2.2],ITDigitDetectionEvent interface, tapi3.itdigitdetectionevent_get_digit, tapi3if/ITDigitDetectionEvent::get_Digit
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
 - ITDigitDetectionEvent.get_Digit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDigitDetectionEvent::get_Digit


## -description


The 
<b>get_Digit</b> method retrieves an unsigned char pointer to the digit that was detected.


## -parameters




### -param pucDigit [out]

Pointer to the digit.


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
The <i>pucDigit</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f387f5f5-06e4-45f2-8d93-31ff0da6151a">ITDigitDetectionEvent</a>
 

 

