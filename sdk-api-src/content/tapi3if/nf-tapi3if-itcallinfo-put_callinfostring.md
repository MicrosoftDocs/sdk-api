---
UID: NF:tapi3if.ITCallInfo.put_CallInfoString
title: ITCallInfo::put_CallInfoString (tapi3if.h)
description: The put_CallInfoString method sets call information items described by a string, such as the displayable address.
helpviewer_keywords: ["ITCallInfo interface [TAPI 2.2]","put_CallInfoString method","ITCallInfo.put_CallInfoString","ITCallInfo::put_CallInfoString","_tapi3_itcallinfo_put_callinfostring","put_CallInfoString","put_CallInfoString method [TAPI 2.2]","put_CallInfoString method [TAPI 2.2]","ITCallInfo interface","tapi3.itcallinfo_put_callinfostring","tapi3if/ITCallInfo::put_CallInfoString"]
old-location: tapi3\itcallinfo_put_callinfostring.htm
tech.root: tapi3
ms.assetid: d22f1afb-e036-40d0-9a7f-61d8d24d2376
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],put_CallInfoString method, ITCallInfo.put_CallInfoString, ITCallInfo::put_CallInfoString, _tapi3_itcallinfo_put_callinfostring, put_CallInfoString, put_CallInfoString method [TAPI 2.2], put_CallInfoString method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_put_callinfostring, tapi3if/ITCallInfo::put_CallInfoString
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
 - ITCallInfo::put_CallInfoString
 - tapi3if/ITCallInfo::put_CallInfoString
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
 - ITCallInfo.put_CallInfoString
---

# ITCallInfo::put_CallInfoString


## -description

The 
<b>put_CallInfoString</b> method sets call information items described by a string, such as the displayable address.

## -parameters

### -param CallInfoString [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_string">CALLINFO_STRING</a> indicator of information type, such as CIS_DISPLAYABLEADDRESS.

### -param pCallInfoString [in]

Pointer to a BSTR representation of the string.

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
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the string data referenced by <i>pCallInfoString</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_string">CALLINFO_STRING</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring">get_CallInfoString</a>