---
UID: NF:tapi3if.ITAddressTranslation.EnumerateCallingCards
title: ITAddressTranslation::EnumerateCallingCards (tapi3if.h)
author: windows-sdk-content
description: The EnumerateCallingCards method enumerates calling cards associated with the address. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_CallingCards method.
old-location: tapi3\itaddresstranslation_enumeratecallingcards.htm
tech.root: Tapi
ms.assetid: 93f3cea1-70da-41f0-a8d5-692468a21695
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumerateCallingCards, EnumerateCallingCards method [TAPI 2.2], EnumerateCallingCards method [TAPI 2.2],ITAddressTranslation interface, ITAddressTranslation interface [TAPI 2.2],EnumerateCallingCards method, ITAddressTranslation.EnumerateCallingCards, ITAddressTranslation::EnumerateCallingCards, _tapi3_itaddresstranslation_enumeratecallingcards, tapi3.itaddresstranslation_enumeratecallingcards, tapi3if/ITAddressTranslation::EnumerateCallingCards
ms.topic: method
f1_keywords: 
 - "tapi3if/ITAddressTranslation.EnumerateCallingCards"
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
 - ITAddressTranslation.EnumerateCallingCards
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAddressTranslation::EnumerateCallingCards


## -description


The 
<b>EnumerateCallingCards</b> method enumerates calling cards associated with the address. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-get_callingcards">get_CallingCards</a> method.


## -parameters




### -param ppEnumCallingCard [out]

Pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard">IEnumCallingCard</a> interface.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnumCallingCard</i> parameter is not a valid pointer.

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



This method is a COM wrapper for the TAPI 2.1 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">LineGetTranslateCaps</a> function, and takes calling card information from the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure returned by that function.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard">IEnumCallingCard</a> interface returned by <b>ITAddressTranslation::EnumerateCallingCards</b>. The application must call <b>Release</b> on the 
<b>IEnumCallingCard</b> interface to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard">IEnumCallingCard</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation">ITAddressTranslation</a>
 

 

