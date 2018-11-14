---
UID: NF:tapi3if.ITLegacyCallMediaControl.DetectDigits
title: ITLegacyCallMediaControl::DetectDigits
author: windows-sdk-content
description: The DetectDigits method sets an identifier of the type of digits that will be detected on the current call, such as rotary pulse or DTMF.
old-location: tapi3\itlegacycallmediacontrol_detectdigits.htm
tech.root: tapi
ms.assetid: 09adb3fb-cf77-4c8b-beab-85d173cbb242
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DetectDigits, DetectDigits method [TAPI 2.2], DetectDigits method [TAPI 2.2],ITLegacyCallMediaControl interface, ITLegacyCallMediaControl interface [TAPI 2.2],DetectDigits method, ITLegacyCallMediaControl.DetectDigits, ITLegacyCallMediaControl::DetectDigits, _tapi3_itlegacycallmediacontrol_detectdigits, tapi3.itlegacycallmediacontrol_detectdigits, tapi3if/ITLegacyCallMediaControl::DetectDigits
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
 - ITLegacyCallMediaControl.DetectDigits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITLegacyCallMediaControl.DetectDigits
: 
---

# ITLegacyCallMediaControl::DetectDigits


## -description


The 
<b>DetectDigits</b> method sets an identifier of the type of digits that will be detected on the current call, such as rotary pulse or DTMF.


## -parameters




### -param DigitMode [in]

Indicates 
<a href="https://msdn.microsoft.com/69663f27-10e6-4dc1-bcab-728c83648912">digit mode</a>.


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
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
No call currently exists.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8">ITLegacyAddressMediaControl</a>



<a href="https://msdn.microsoft.com/73288c46-6c6d-4938-9bb7-4d94acfc67f6">ITLegacyCallMediaControl</a>
 

 

