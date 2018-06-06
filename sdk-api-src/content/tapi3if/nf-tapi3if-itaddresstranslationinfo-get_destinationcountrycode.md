---
UID: NF:tapi3if.ITAddressTranslationInfo.get_DestinationCountryCode
title: ITAddressTranslationInfo::get_DestinationCountryCode
author: windows-sdk-content
description: Retrieves the country/region code for the call destination.
old-location: tapi3\itaddresstranslationinfo_get_destinationcountrycode.htm
old-project: Tapi
ms.assetid: 29880773-ce19-489f-81d8-d2c91779350f
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITAddressTranslationInfo interface [TAPI 2.2],get_DestinationCountryCode method, ITAddressTranslationInfo.get_DestinationCountryCode, ITAddressTranslationInfo::get_DestinationCountryCode, _tapi3_itaddresstranslationinfo_get_destinationcountrycode, get_DestinationCountryCode, get_DestinationCountryCode method [TAPI 2.2], get_DestinationCountryCode method [TAPI 2.2],ITAddressTranslationInfo interface, tapi3.itaddresstranslationinfo_get_destinationcountrycode, tapi3if/ITAddressTranslationInfo::get_DestinationCountryCode
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
 - ITAddressTranslationInfo.get_DestinationCountryCode
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddressTranslationInfo::get_DestinationCountryCode


## -description


The 
<b>get_DestinationCountryCode</b> method retrieves the country/region code for the call destination.


## -parameters




### -param CountryCode [out]

A pointer to destination country/region code.


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
The <i>CountryCode</i> parameter is an invalid pointer.

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



Corresponds to the <b>dwDestCountry</b> member of the TAPI 2 
<a href="https://msdn.microsoft.com/bcf094ad-8098-4e45-9131-25dbdb7e4093">LINETRANSLATEOUTPUT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a>
 

 

