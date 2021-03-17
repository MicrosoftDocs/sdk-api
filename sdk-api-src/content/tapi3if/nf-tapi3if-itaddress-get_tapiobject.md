---
UID: NF:tapi3if.ITAddress.get_TAPIObject
title: ITAddress::get_TAPIObject (tapi3if.h)
description: The get_TAPIObject method gets a pointer to the TAPI object that owns this address.
helpviewer_keywords: ["ITAddress interface [TAPI 2.2]","get_TAPIObject method","ITAddress.get_TAPIObject","ITAddress::get_TAPIObject","_tapi3_itaddress_get_tapiobject","get_TAPIObject","get_TAPIObject method [TAPI 2.2]","get_TAPIObject method [TAPI 2.2]","ITAddress interface","tapi3.itaddress_get_tapiobject","tapi3if/ITAddress::get_TAPIObject"]
old-location: tapi3\itaddress_get_tapiobject.htm
tech.root: tapi3
ms.assetid: 37064bef-d5c0-44b9-a7eb-ae922b175f91
ms.date: 12/05/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_TAPIObject method, ITAddress.get_TAPIObject, ITAddress::get_TAPIObject, _tapi3_itaddress_get_tapiobject, get_TAPIObject, get_TAPIObject method [TAPI 2.2], get_TAPIObject method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_tapiobject, tapi3if/ITAddress::get_TAPIObject
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
 - ITAddress::get_TAPIObject
 - tapi3if/ITAddress::get_TAPIObject
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
 - ITAddress.get_TAPIObject
---

# ITAddress::get_TAPIObject


## -description

The 
<b>get_TAPIObject</b> method gets a pointer to the TAPI object that owns this address.

## -parameters

### -param ppTapiObject [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a> interface.

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
The <i>ppTapiObject</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>