---
UID: NF:tapi3if.ITCallInfo.GetCallInfoBuffer
title: ITCallInfo::GetCallInfoBuffer (tapi3if.h)
description: The GetCallInfoBuffer method gets call information items that require a buffer, such as user-user information. Automation client applications, such as those written in Visual Basic, must use the ITCallInfo::get_CallInfoBuffer method.
helpviewer_keywords: ["GetCallInfoBuffer","GetCallInfoBuffer method [TAPI 2.2]","GetCallInfoBuffer method [TAPI 2.2]","ITCallInfo interface","ITCallInfo interface [TAPI 2.2]","GetCallInfoBuffer method","ITCallInfo.GetCallInfoBuffer","ITCallInfo::GetCallInfoBuffer","_tapi3_itcallinfo_getcallinfobuffer","tapi3.itcallinfo_getcallinfobuffer","tapi3if/ITCallInfo::GetCallInfoBuffer"]
old-location: tapi3\itcallinfo_getcallinfobuffer.htm
tech.root: tapi3
ms.assetid: 00f5dde6-e9df-4b61-8122-2183e047f9ba
ms.date: 12/05/2018
ms.keywords: GetCallInfoBuffer, GetCallInfoBuffer method [TAPI 2.2], GetCallInfoBuffer method [TAPI 2.2],ITCallInfo interface, ITCallInfo interface [TAPI 2.2],GetCallInfoBuffer method, ITCallInfo.GetCallInfoBuffer, ITCallInfo::GetCallInfoBuffer, _tapi3_itcallinfo_getcallinfobuffer, tapi3.itcallinfo_getcallinfobuffer, tapi3if/ITCallInfo::GetCallInfoBuffer
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
 - ITCallInfo::GetCallInfoBuffer
 - tapi3if/ITCallInfo::GetCallInfoBuffer
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
 - ITCallInfo.GetCallInfoBuffer
---

# ITCallInfo::GetCallInfoBuffer


## -description

The 
<b>GetCallInfoBuffer</b> method gets call information items that require a buffer, such as user-user information. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer">ITCallInfo::get_CallInfoBuffer</a> method.

## -parameters

### -param CallInfoBuffer [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_buffer">CALLINFO_BUFFER</a> indicator of information type needed, such as CIB_USERUSERINFO.

### -param pdwSize [out]

Size of buffer returned in bytes.

### -param ppCallInfoBuffer [out]

Pointer to buffer containing the needed call information.

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
The <i>pdwSize</i> or <i>ppCallInfoBuffer</i> parameter is not a valid pointer.

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



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-setcallinfobuffer">SetCallInfoBuffer</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer">get_CallInfoBuffer</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer">put_CallInfoBuffer</a>