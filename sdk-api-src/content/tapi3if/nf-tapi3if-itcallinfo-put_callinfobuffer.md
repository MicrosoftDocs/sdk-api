---
UID: NF:tapi3if.ITCallInfo.put_CallInfoBuffer
title: ITCallInfo::put_CallInfoBuffer (tapi3if.h)
description: The put_CallInfoBuffer method sets call information items which require a buffer, such as user-user information.
helpviewer_keywords: ["ITCallInfo interface [TAPI 2.2]","put_CallInfoBuffer method","ITCallInfo.put_CallInfoBuffer","ITCallInfo::put_CallInfoBuffer","_tapi3_itcallinfo_put_callinfobuffer","put_CallInfoBuffer","put_CallInfoBuffer method [TAPI 2.2]","put_CallInfoBuffer method [TAPI 2.2]","ITCallInfo interface","tapi3.itcallinfo_put_callinfobuffer","tapi3if/ITCallInfo::put_CallInfoBuffer"]
old-location: tapi3\itcallinfo_put_callinfobuffer.htm
tech.root: tapi3
ms.assetid: 4404ec08-2443-4d1a-8f94-5eb1b3315169
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],put_CallInfoBuffer method, ITCallInfo.put_CallInfoBuffer, ITCallInfo::put_CallInfoBuffer, _tapi3_itcallinfo_put_callinfobuffer, put_CallInfoBuffer, put_CallInfoBuffer method [TAPI 2.2], put_CallInfoBuffer method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_put_callinfobuffer, tapi3if/ITCallInfo::put_CallInfoBuffer
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
 - ITCallInfo::put_CallInfoBuffer
 - tapi3if/ITCallInfo::put_CallInfoBuffer
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
 - ITCallInfo.put_CallInfoBuffer
---

# ITCallInfo::put_CallInfoBuffer


## -description

The 
<b>put_CallInfoBuffer</b> method sets call information items which require a buffer, such as user-user information. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-setcallinfobuffer">ITCallInfo::SetCallInfoBuffer</a> method.

## -parameters

### -param CallInfoBuffer [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_buffer">CALLINFO_BUFFER</a> indicator of information type, such as CIB_USERUSERINFO.

### -param pCallInfoBuffer [in]

<b>VARIANT</b>

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



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer">get_CallInfoBuffer</a>