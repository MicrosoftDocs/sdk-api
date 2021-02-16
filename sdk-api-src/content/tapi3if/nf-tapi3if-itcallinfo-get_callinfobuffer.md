---
UID: NF:tapi3if.ITCallInfo.get_CallInfoBuffer
title: ITCallInfo::get_CallInfoBuffer (tapi3if.h)
description: The get_CallInfoBuffer method gets call information items which require a buffer, such as user-user information.
helpviewer_keywords: ["ITCallInfo interface [TAPI 2.2]","get_CallInfoBuffer method","ITCallInfo.get_CallInfoBuffer","ITCallInfo::get_CallInfoBuffer","_tapi3_itcallinfo_get_callinfobuffer","get_CallInfoBuffer","get_CallInfoBuffer method [TAPI 2.2]","get_CallInfoBuffer method [TAPI 2.2]","ITCallInfo interface","tapi3.itcallinfo_get_callinfobuffer","tapi3if/ITCallInfo::get_CallInfoBuffer"]
old-location: tapi3\itcallinfo_get_callinfobuffer.htm
tech.root: tapi3
ms.assetid: cda9d577-7230-42d9-8063-5ca94e0400dc
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_CallInfoBuffer method, ITCallInfo.get_CallInfoBuffer, ITCallInfo::get_CallInfoBuffer, _tapi3_itcallinfo_get_callinfobuffer, get_CallInfoBuffer, get_CallInfoBuffer method [TAPI 2.2], get_CallInfoBuffer method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_callinfobuffer, tapi3if/ITCallInfo::get_CallInfoBuffer
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
 - ITCallInfo::get_CallInfoBuffer
 - tapi3if/ITCallInfo::get_CallInfoBuffer
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
 - ITCallInfo.get_CallInfoBuffer
---

# ITCallInfo::get_CallInfoBuffer


## -description

The 
<b>get_CallInfoBuffer</b> method gets call information items which require a buffer, such as user-user information. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer">ITCallInfo::GetCallInfoBuffer</a> method.

## -parameters

### -param CallInfoBuffer [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_buffer">CALLINFO_BUFFER</a> indicator of information type needed, such as CIB_USERUSERINFO.

### -param ppCallInfoBuffer [out]

Pointer to <b>VARIANT</b> representation of call information buffer. The application must call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free the memory allocated for this parameter.

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
The <i>ppCallInfoBuffer</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>CallInfoBuffer</i> parameter is not a valid value.

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

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_buffer">CALLINFO_BUFFER</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer">GetCallInfoBuffer</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-setcallinfobuffer">SetCallInfoBuffer</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer">put_CallInfoBuffer</a>