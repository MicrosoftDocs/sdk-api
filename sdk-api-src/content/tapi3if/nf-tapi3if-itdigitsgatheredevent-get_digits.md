---
UID: NF:tapi3if.ITDigitsGatheredEvent.get_Digits
title: ITDigitsGatheredEvent::get_Digits
author: windows-driver-content
description: The get_Digits method gets the gathered digits for the call.
old-location: tapi3\itdigitsgatheredevent_get_digits.htm
old-project: Tapi
ms.assetid: 940e186b-33bd-4846-8314-39ede19bad95
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITDigitsGatheredEvent interface [TAPI 2.2],get_Digits method, ITDigitsGatheredEvent.get_Digits, ITDigitsGatheredEvent::get_Digits, _tapi3_itdigitsgatheredevent_get_digits, get_Digits, get_Digits method [TAPI 2.2], get_Digits method [TAPI 2.2],ITDigitsGatheredEvent interface, tapi3.itdigitsgatheredevent_get_digits, tapi3if/ITDigitsGatheredEvent::get_Digits
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITDigitsGatheredEvent.get_Digits
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITDigitsGatheredEvent::get_Digits


## -description


The 
<b>get_Digits</b> method gets the gathered digits for the call.


## -parameters




### -param ppDigits [out]

Pointer to a <b>BSTR</b> where the gathered digits are stored.


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
The <i>ppDigits</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2d710bea-a0fd-492b-81a3-03b741685c91">ITDigitsGatheredEvent</a>
 

 

