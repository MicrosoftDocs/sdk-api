---
UID: NF:tapi3if.ITAddressTranslationInfo.get_CurrentCountryCode
title: ITAddressTranslationInfo::get_CurrentCountryCode
author: windows-sdk-content
description: The get_CurrentCountryCode method gets the current country/region code.
old-location: tapi3\itaddresstranslationinfo_get_currentcountrycode.htm
old-project: tapi
ms.assetid: 02b19558-d7cb-4c77-977b-9810468ff145
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITAddressTranslationInfo interface [TAPI 2.2],get_CurrentCountryCode method, ITAddressTranslationInfo.get_CurrentCountryCode, ITAddressTranslationInfo::get_CurrentCountryCode, _tapi3_itaddresstranslationinfo_get_currentcountrycode, get_CurrentCountryCode, get_CurrentCountryCode method [TAPI 2.2], get_CurrentCountryCode method [TAPI 2.2],ITAddressTranslationInfo interface, tapi3.itaddresstranslationinfo_get_currentcountrycode, tapi3if/ITAddressTranslationInfo::get_CurrentCountryCode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddressTranslationInfo.get_CurrentCountryCode
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddressTranslationInfo::get_CurrentCountryCode


## -description


The 
<b>get_CurrentCountryCode</b> method gets the current country/region code.


## -parameters




### -param CountryCode [out]

Pointer to the country/region code.


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
The <i>CountryCode</i> parameter is not a valid pointer.

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



Corresponds to the <b>dwCurrentCountry</b> member of the TAPI 2 
<a href="https://msdn.microsoft.com/bcf094ad-8098-4e45-9131-25dbdb7e4093">LINETRANSLATEOUTPUT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a>
 

 

