---
UID: NF:tapi3if.ITForwardInformation.SetForwardType
title: ITForwardInformation::SetForwardType (tapi3if.h)
description: The SetForwardType method sets the forwarding mode and destination by caller address.
helpviewer_keywords: ["ITForwardInformation interface [TAPI 2.2]","SetForwardType method","ITForwardInformation.SetForwardType","ITForwardInformation::SetForwardType","SetForwardType","SetForwardType method [TAPI 2.2]","SetForwardType method [TAPI 2.2]","ITForwardInformation interface","_tapi3_itforwardinformation_setforwardtype","tapi3.itforwardinformation_setforwardtype","tapi3if/ITForwardInformation::SetForwardType"]
old-location: tapi3\itforwardinformation_setforwardtype.htm
tech.root: tapi3
ms.assetid: 5f7972a8-c9b0-4033-8b00-a107a513ee66
ms.date: 12/05/2018
ms.keywords: ITForwardInformation interface [TAPI 2.2],SetForwardType method, ITForwardInformation.SetForwardType, ITForwardInformation::SetForwardType, SetForwardType, SetForwardType method [TAPI 2.2], SetForwardType method [TAPI 2.2],ITForwardInformation interface, _tapi3_itforwardinformation_setforwardtype, tapi3.itforwardinformation_setforwardtype, tapi3if/ITForwardInformation::SetForwardType
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
 - ITForwardInformation::SetForwardType
 - tapi3if/ITForwardInformation::SetForwardType
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
 - ITForwardInformation.SetForwardType
---

# ITForwardInformation::SetForwardType


## -description

The 
<b>SetForwardType</b> method sets the forwarding mode and destination by caller address.

## -parameters

### -param ForwardType [in]

<a href="/windows/desktop/Tapi/lineforwardmode--constants">Line forward mode</a>.

### -param pDestAddress [in]

Pointer to <b>BSTR</b> representation of destination address for forwarding.

### -param pCallerAddress [in]

Pointer to <b>BSTR</b> representation of caller address.

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
The <i>pDestAddress</i> or <i>pCallerAddress</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ForwardType</i> parameter is not valid.

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
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pDestAddress</i> and <i>pCallerAddress</i> parameters. The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variables are no longer needed.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">ITAddress::Forward</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>