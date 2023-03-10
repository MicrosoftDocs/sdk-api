---
UID: NF:tapi3if.ITCallInfo.get_CallInfoString
title: ITCallInfo::get_CallInfoString (tapi3if.h)
description: The get_CallInfoString method gets call information items described by a string, such as the displayable address.
helpviewer_keywords: ["ITCallInfo interface [TAPI 2.2]","get_CallInfoString method","ITCallInfo.get_CallInfoString","ITCallInfo::get_CallInfoString","_tapi3_itcallinfo_get_callinfostring","get_CallInfoString","get_CallInfoString method [TAPI 2.2]","get_CallInfoString method [TAPI 2.2]","ITCallInfo interface","tapi3.itcallinfo_get_callinfostring","tapi3if/ITCallInfo::get_CallInfoString"]
old-location: tapi3\itcallinfo_get_callinfostring.htm
tech.root: tapi3
ms.assetid: 248022e7-c6cf-4c46-be94-ee1b79b9f39a
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_CallInfoString method, ITCallInfo.get_CallInfoString, ITCallInfo::get_CallInfoString, _tapi3_itcallinfo_get_callinfostring, get_CallInfoString, get_CallInfoString method [TAPI 2.2], get_CallInfoString method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_callinfostring, tapi3if/ITCallInfo::get_CallInfoString
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
 - ITCallInfo::get_CallInfoString
 - tapi3if/ITCallInfo::get_CallInfoString
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
 - ITCallInfo.get_CallInfoString
---

# ITCallInfo::get_CallInfoString


## -description

The 
<b>get_CallInfoString</b> method gets call information items described by a string, such as the displayable address.

## -parameters

### -param CallInfoString [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_string">CALLINFO_STRING</a> indicator of information type needed, such as CIS_DISPLAYABLEADDRESS.

### -param ppCallInfoString [out]

Pointer to <b>BSTR</b> representation of needed string.

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
The <i>ppCallInfoString</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>CallInfoString</i> parameter is not a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
The current 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">call state</a> is not valid for this operation.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppCallInfoString</i> parameter.

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_string">CALLINFO_STRING</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfostring">put_CallInfoString</a>