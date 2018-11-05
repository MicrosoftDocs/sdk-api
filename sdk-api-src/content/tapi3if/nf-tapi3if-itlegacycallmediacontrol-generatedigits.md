---
UID: NF:tapi3if.ITLegacyCallMediaControl.GenerateDigits
title: ITLegacyCallMediaControl::GenerateDigits
author: windows-sdk-content
description: The GenerateDigits method causes digits to be output on the current call.
old-location: tapi3\itlegacycallmediacontrol_generatedigits.htm
tech.root: tapi
ms.assetid: d4dcdce0-4df5-43bb-a5ea-ea72782d5f04
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GenerateDigits, GenerateDigits method [TAPI 2.2], GenerateDigits method [TAPI 2.2],ITLegacyCallMediaControl interface, ITLegacyCallMediaControl interface [TAPI 2.2],GenerateDigits method, ITLegacyCallMediaControl.GenerateDigits, ITLegacyCallMediaControl::GenerateDigits, _tapi3_itlegacycallmediacontrol_generatedigits, tapi3.itlegacycallmediacontrol_generatedigits, tapi3if/ITLegacyCallMediaControl::GenerateDigits
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
 - ITLegacyCallMediaControl.GenerateDigits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyCallMediaControl::GenerateDigits


## -description


The 
<b>GenerateDigits</b> method causes digits to be output on the current call.


## -parameters




### -param pDigits [in]

Pointer to <b>BSTR</b> representation of digits to be sent.


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
 




## -remarks



The application must use 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pDigits</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8">ITLegacyAddressMediaControl</a>



<a href="https://msdn.microsoft.com/73288c46-6c6d-4938-9bb7-4d94acfc67f6">ITLegacyCallMediaControl</a>
 

 

