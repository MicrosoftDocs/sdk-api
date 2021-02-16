---
UID: NF:tapi3if.ITAddress.get_AddressName
title: ITAddress::get_AddressName (tapi3if.h)
description: The get_AddressName method gets the displayable name of the address.
helpviewer_keywords: ["ITAddress interface [TAPI 2.2]","get_AddressName method","ITAddress.get_AddressName","ITAddress::get_AddressName","_tapi3_itaddress_get_addressname","get_AddressName","get_AddressName method [TAPI 2.2]","get_AddressName method [TAPI 2.2]","ITAddress interface","tapi3.itaddress_get_addressname","tapi3if/ITAddress::get_AddressName"]
old-location: tapi3\itaddress_get_addressname.htm
tech.root: tapi3
ms.assetid: cb26dcf5-0192-4156-914b-9aa6e76a2bd2
ms.date: 12/05/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_AddressName method, ITAddress.get_AddressName, ITAddress::get_AddressName, _tapi3_itaddress_get_addressname, get_AddressName, get_AddressName method [TAPI 2.2], get_AddressName method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_addressname, tapi3if/ITAddress::get_AddressName
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
 - ITAddress::get_AddressName
 - tapi3if/ITAddress::get_AddressName
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
 - ITAddress.get_AddressName
---

# ITAddress::get_AddressName


## -description

The 
<b>get_AddressName</b> method gets the displayable name of the address.

## -parameters

### -param ppName [out]

Pointer to <b>BSTR</b> containing a displayable address name.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppName</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppName</i> parameter.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>