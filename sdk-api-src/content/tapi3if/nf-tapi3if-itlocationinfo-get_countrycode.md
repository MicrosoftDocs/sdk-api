---
UID: NF:tapi3if.ITLocationInfo.get_CountryCode
title: ITLocationInfo::get_CountryCode
author: windows-sdk-content
description: The get_CountryCode method gets the country/region code.
old-location: tapi3\itlocationinfo_get_countrycode.htm
tech.root: tapi
ms.assetid: 3ddd2e25-39ac-419b-9f99-85c6086f0377
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_CountryCode method, ITLocationInfo.get_CountryCode, ITLocationInfo::get_CountryCode, _tapi3_itlocationinfo_get_countrycode, get_CountryCode, get_CountryCode method [TAPI 2.2], get_CountryCode method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_countrycode, tapi3if/ITLocationInfo::get_CountryCode
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
 - ITLocationInfo.get_CountryCode
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
- ITLocationInfo.get_CountryCode
: 
---

# ITLocationInfo::get_CountryCode


## -description


The 
<b>get_CountryCode</b> method gets the country/region code.


## -parameters




### -param plCountryCode [out]

Pointer to country/region code.


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
The <i>plCountryCode</i> parameter is not a valid pointer.

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
 




## -remarks



The value that this method returns corresponds to the <b>dwCountryCode</b> member of TAPI 2's 
<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a>



<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>
 

 

