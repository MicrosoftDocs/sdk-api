---
UID: NF:tapi3if.ITAddress.get_DialableAddress
title: ITAddress::get_DialableAddress (tapi3if.h)
description: The get_DialableAddress method gets the BSTR which can be used to connect to this address. The BSTR corresponds to the destination address string that another application would use to connect to this address, such as a phone number or an e-mail name.
helpviewer_keywords: ["ITAddress interface [TAPI 2.2]","get_DialableAddress method","ITAddress.get_DialableAddress","ITAddress::get_DialableAddress","_tapi3_itaddress_get_dialableaddress","get_DialableAddress","get_DialableAddress method [TAPI 2.2]","get_DialableAddress method [TAPI 2.2]","ITAddress interface","tapi3.itaddress_get_dialableaddress","tapi3if/ITAddress::get_DialableAddress"]
old-location: tapi3\itaddress_get_dialableaddress.htm
tech.root: tapi3
ms.assetid: 8d6dcbbe-3372-4346-8f5e-fb34b7aca88d
ms.date: 12/05/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_DialableAddress method, ITAddress.get_DialableAddress, ITAddress::get_DialableAddress, _tapi3_itaddress_get_dialableaddress, get_DialableAddress, get_DialableAddress method [TAPI 2.2], get_DialableAddress method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_dialableaddress, tapi3if/ITAddress::get_DialableAddress
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAddress::get_DialableAddress
 - tapi3if/ITAddress::get_DialableAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddress.get_DialableAddress
---

# ITAddress::get_DialableAddress


## -description

The 
<b>get_DialableAddress</b> method gets the <b>BSTR</b> which can be used to connect to this address. The <b>BSTR</b> corresponds to the destination address string that another application would use to connect to this address, such as a phone number or an e-mail name.

## -parameters

### -param pDialableAddress [out]

Pointer to <b>BSTR</b> containing the dialable address string. This will match the <i>pDestAddress</i> argument of 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>.

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
The <i>pDialableAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>pDialableAddress</i> parameter.
			

The availability of this value depends on the service provider. For example, on an address exposed by the Unimodem service provider, this method will return an empty string instead of a phone number.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/Tapi/address-ovr">Dialable Addresses</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>