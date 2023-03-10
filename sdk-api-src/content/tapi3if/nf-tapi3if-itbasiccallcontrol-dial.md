---
UID: NF:tapi3if.ITBasicCallControl.Dial
title: ITBasicCallControl::Dial (tapi3if.h)
description: The Dial method dials the specified address.
helpviewer_keywords: ["Dial","Dial method [TAPI 2.2]","Dial method [TAPI 2.2]","ITBasicCallControl interface","ITBasicCallControl interface [TAPI 2.2]","Dial method","ITBasicCallControl.Dial","ITBasicCallControl::Dial","_tapi3_itbasiccallcontrol_dial","tapi3.itbasiccallcontrol_dial","tapi3if/ITBasicCallControl::Dial"]
old-location: tapi3\itbasiccallcontrol_dial.htm
tech.root: tapi3
ms.assetid: 31fea4d8-9028-48d5-9f5d-53f1451103c7
ms.date: 12/05/2018
ms.keywords: Dial, Dial method [TAPI 2.2], Dial method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],Dial method, ITBasicCallControl.Dial, ITBasicCallControl::Dial, _tapi3_itbasiccallcontrol_dial, tapi3.itbasiccallcontrol_dial, tapi3if/ITBasicCallControl::Dial
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
 - ITBasicCallControl::Dial
 - tapi3if/ITBasicCallControl::Dial
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
 - ITBasicCallControl.Dial
---

# ITBasicCallControl::Dial


## -description

The 
<b>Dial</b> method dials the specified address.

## -parameters

### -param pDestAddress [in]

Pointer to <b>BSTR</b> representation of address to be dialed. The format must conform to a standard 
<a href="/windows/desktop/Tapi/address-ovr">dialable address</a>.

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
The <i>pDestAddress</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pDestAddress</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

In some cases, the application may need to use the address translation interfaces (
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation">ITAddressTranslation</a> and 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a>) to obtain a <i>pDestAddress</i> string in the proper format.

The 
<b>Dial</b> method differs from 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a> in that the call already exists. An example use is dialing an extension.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/Tapi/dial-ovr">Dial overview</a>



<a href="/windows/desktop/Tapi/address-ovr">Dialable Addresses</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation">ITAddressTranslation</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linedial">lineDial</a>