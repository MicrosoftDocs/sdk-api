---
UID: NF:tapi3if.ITForwardInformation2.get_ForwardTypeCallerAddressType
title: ITForwardInformation2::get_ForwardTypeCallerAddressType (tapi3if.h)
description: The get_ForwardTypeCallerAddressType method gets the caller address type for a given forwarding type.
helpviewer_keywords: ["ITForwardInformation2 interface [TAPI 2.2]","get_ForwardTypeCallerAddressType method","ITForwardInformation2.get_ForwardTypeCallerAddressType","ITForwardInformation2::get_ForwardTypeCallerAddressType","_tapi3_itforwardinformation2_get_forwardtypecalleraddresstype","get_ForwardTypeCallerAddressType","get_ForwardTypeCallerAddressType method [TAPI 2.2]","get_ForwardTypeCallerAddressType method [TAPI 2.2]","ITForwardInformation2 interface","tapi3.itforwardinformation2_get_forwardtypecalleraddresstype","tapi3if/ITForwardInformation2::get_ForwardTypeCallerAddressType"]
old-location: tapi3\itforwardinformation2_get_forwardtypecalleraddresstype.htm
tech.root: tapi3
ms.assetid: 030d2b44-0c1d-488b-8cd9-e68ad6d26c6e
ms.date: 12/05/2018
ms.keywords: ITForwardInformation2 interface [TAPI 2.2],get_ForwardTypeCallerAddressType method, ITForwardInformation2.get_ForwardTypeCallerAddressType, ITForwardInformation2::get_ForwardTypeCallerAddressType, _tapi3_itforwardinformation2_get_forwardtypecalleraddresstype, get_ForwardTypeCallerAddressType, get_ForwardTypeCallerAddressType method [TAPI 2.2], get_ForwardTypeCallerAddressType method [TAPI 2.2],ITForwardInformation2 interface, tapi3.itforwardinformation2_get_forwardtypecalleraddresstype, tapi3if/ITForwardInformation2::get_ForwardTypeCallerAddressType
req.header: tapi3if.h
req.include-header: 
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
 - ITForwardInformation2::get_ForwardTypeCallerAddressType
 - tapi3if/ITForwardInformation2::get_ForwardTypeCallerAddressType
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
 - ITForwardInformation2.get_ForwardTypeCallerAddressType
---

# ITForwardInformation2::get_ForwardTypeCallerAddressType


## -description

The 
<b>get_ForwardTypeCallerAddressType</b> method gets the caller address type for a given forwarding type.

## -parameters

### -param Forwardtype [in]

<a href="/windows/desktop/Tapi/lineforwardmode--constants">Line forward type</a> to be retrieved.

### -param pCallerAddressType [out]

<a href="/windows/desktop/Tapi/lineaddresstype--constants">Address type</a> of the caller.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>Forwardtype</i> parameter is invalid.

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
The <i>pCallerAddressType</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation2">ITForwardInformation2</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation-getforwardtype">ITForwardInformation::GetForwardType</a>