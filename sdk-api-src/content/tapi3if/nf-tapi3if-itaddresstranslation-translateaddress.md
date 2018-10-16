---
UID: NF:tapi3if.ITAddressTranslation.TranslateAddress
title: ITAddressTranslation::TranslateAddress
author: windows-sdk-content
description: The TranslateAddress method creates the address translation information interface.
old-location: tapi3\itaddresstranslation_translateaddress.htm
tech.root: TAPI
ms.assetid: 14e51de8-33fd-4de0-bc1c-5f8085ea095c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITAddressTranslation interface [TAPI 2.2],TranslateAddress method, ITAddressTranslation.TranslateAddress, ITAddressTranslation::TranslateAddress, TranslateAddress, TranslateAddress method [TAPI 2.2], TranslateAddress method [TAPI 2.2],ITAddressTranslation interface, _tapi3_itaddresstranslation_translateaddress, tapi3.itaddresstranslation_translateaddress, tapi3if/ITAddressTranslation::TranslateAddress
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
 - ITAddressTranslation.TranslateAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddressTranslation::TranslateAddress


## -description


The 
<b>TranslateAddress</b> method creates the address translation information interface. The primary goal of the 
<b>TranslateAddress</b> method is to obtain the <i>pDestAddress</i> string (<a href="address_ovr.htm">dialable address</a>) needed as a parameter for 
<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a>. The 
<b>TranslateAddress</b> method returns the dialable address indirectly, as one of the properties of an 
<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a> object.


## -parameters




### -param pAddressToTranslate [in]

Pointer to <b>BSTR</b> containing address that requires translation.


### -param lCard [in]

Calling card used for translation.


### -param lTranslateOptions [in]

Indicator of translation options, see 
<a href="https://msdn.microsoft.com/3f5e9952-945e-42b8-8536-b52a0c833282">LINETRANSLATEOPTION__Constants</a>.


### -param ppTranslated [out]

Pointer to newly created 
<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a> interface.


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
The <i>ppTranslated</i> parameter is not a valid pointer.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for unknown reasons.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lTranslateOptions</i> value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
This address has no TSP associated with it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_REGISTRY_SETTING_CORRUPT</b></dt>
</dl>
</td>
<td width="60%">
The registry is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_OPERATIONFAILED</b></dt>
</dl>
</td>
<td width="60%">
The method failed with TAPI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_RESOURCEUNAVAIL</b></dt>
</dl>
</td>
<td width="60%">
The TSP is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCARD</b></dt>
</dl>
</td>
<td width="60%">
The card number is not valid.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for <i>pAddressToTranslate</i> and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

The 
<b>TranslateAddress</b> method is a COM wrapper for the TAPI 2.1 
<a href="https://msdn.microsoft.com/0347d526-9596-4b42-8075-07318bf39634">LineTranslateAddress</a> function.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a> interface returned by <b>TranslateAddress</b>. The application must call <b>Release</b> on the 
<b>ITAddressTranslationInfo</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="address_ovr.htm">Dialable Addresses</a>



<a href="https://msdn.microsoft.com/e1cd88f1-1ed7-4e7f-a745-9a9c4af69317">ITAddressTranslation</a>
 

 

