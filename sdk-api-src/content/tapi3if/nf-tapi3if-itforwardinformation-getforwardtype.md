---
UID: NF:tapi3if.ITForwardInformation.GetForwardType
title: ITForwardInformation::GetForwardType (tapi3if.h)
description: The GetForwardType method gets the forwarding mode.
helpviewer_keywords: ["GetForwardType","GetForwardType method [TAPI 2.2]","GetForwardType method [TAPI 2.2]","ITForwardInformation interface","ITForwardInformation interface [TAPI 2.2]","GetForwardType method","ITForwardInformation.GetForwardType","ITForwardInformation::GetForwardType","_tapi3_itforwardinformation_getforwardtype","tapi3.itforwardinformation_getforwardtype","tapi3if/ITForwardInformation::GetForwardType"]
old-location: tapi3\itforwardinformation_getforwardtype.htm
tech.root: tapi3
ms.assetid: 02d3c558-585a-4dcc-873e-8465c1d2af64
ms.date: 12/05/2018
ms.keywords: GetForwardType, GetForwardType method [TAPI 2.2], GetForwardType method [TAPI 2.2],ITForwardInformation interface, ITForwardInformation interface [TAPI 2.2],GetForwardType method, ITForwardInformation.GetForwardType, ITForwardInformation::GetForwardType, _tapi3_itforwardinformation_getforwardtype, tapi3.itforwardinformation_getforwardtype, tapi3if/ITForwardInformation::GetForwardType
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
 - ITForwardInformation::GetForwardType
 - tapi3if/ITForwardInformation::GetForwardType
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
 - ITForwardInformation.GetForwardType
---

# ITForwardInformation::GetForwardType


## -description

The 
<b>GetForwardType</b> method gets the forwarding mode.

## -parameters

### -param ForwardType [in]

<a href="/windows/desktop/Tapi/lineforwardmode--constants">Line forward mode</a>.

### -param ppDestinationAddress [out]

Pointer to <b>BSTR</b> representation of destination address.

### -param ppCallerAddress [out]

Pointer to <b>BSTR</b> representation of the call originator's address.

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
The <i>ppDestAddress</i> or <i>ppCallerAddress</i> parameter is not a valid pointer.

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

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppDestinationAddress</i> and <i>ppCallerAddress</i> parameters.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">ITAddress::Forward</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation2-getforwardtype2">ITForwardInformation2::GetForwardType</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>