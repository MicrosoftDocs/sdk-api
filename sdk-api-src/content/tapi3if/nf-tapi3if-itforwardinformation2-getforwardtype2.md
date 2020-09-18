---
UID: NF:tapi3if.ITForwardInformation2.GetForwardType2
title: ITForwardInformation2::GetForwardType2 (tapi3if.h)
description: The GetForwardType2 method gets the current forwarding mode, specified by caller address.
helpviewer_keywords: ["GetForwardType2","GetForwardType2 method [TAPI 2.2]","GetForwardType2 method [TAPI 2.2]","ITForwardInformation2 interface","ITForwardInformation2 interface [TAPI 2.2]","GetForwardType2 method","ITForwardInformation2.GetForwardType2","ITForwardInformation2::GetForwardType2","_tapi3_itforwardinformation2_getforwardtype2","tapi3.itforwardinformation2_getforwardtype2","tapi3if/ITForwardInformation2::GetForwardType2"]
old-location: tapi3\itforwardinformation2_getforwardtype2.htm
tech.root: tapi3
ms.assetid: c3142217-d3fa-4e0b-ad3b-65a0557ce951
ms.date: 12/05/2018
ms.keywords: GetForwardType2, GetForwardType2 method [TAPI 2.2], GetForwardType2 method [TAPI 2.2],ITForwardInformation2 interface, ITForwardInformation2 interface [TAPI 2.2],GetForwardType2 method, ITForwardInformation2.GetForwardType2, ITForwardInformation2::GetForwardType2, _tapi3_itforwardinformation2_getforwardtype2, tapi3.itforwardinformation2_getforwardtype2, tapi3if/ITForwardInformation2::GetForwardType2
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
 - ITForwardInformation2::GetForwardType2
 - tapi3if/ITForwardInformation2::GetForwardType2
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
 - ITForwardInformation2.GetForwardType2
---

# ITForwardInformation2::GetForwardType2


## -description

The 
<b>GetForwardType2</b> method gets the current forwarding mode, specified by caller address.

## -parameters

### -param ForwardType [in]

<a href="/windows/desktop/Tapi/lineforwardmode--constants">Line forward type</a> to be retrieved.

### -param ppDestinationAddress [out]

Pointer to the <b>BSTR</b> representation of the destination address.

### -param pDestAddressType [out]

<a href="/windows/desktop/Tapi/lineaddresstype--constants">Address type</a> of the destination.

### -param ppCallerAddress [out]

Pointer to the <b>BSTR</b> representation of the caller address.

### -param pCallerAddressType [out]

<a href="/windows/desktop/Tapi/lineaddresstype--constants">Address type</a> of the caller.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ForwardType</i>, <i>pDestAddressType</i>, or <i>pCallerAddressType</i> parameter is invalid.

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
The <i>ppDestinationAddress</i>, <i>pDestAddressType</i>, <i>pCallerAddressType</i>, or <i>ppCallerAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation2">ITForwardInformation2</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation-getforwardtype">ITForwardInformation::GetForwardType</a>