---
UID: NF:tapi3if.ITCallInfo.SetCallInfoBuffer
title: ITCallInfo::SetCallInfoBuffer (tapi3if.h)
description: The SetCallInfoBuffer method sets call information items that require a buffer, such as user-user information. Automation client applications, such as those written in Visual Basic, must use the ITCallInfo::put_CallInfoBuffer method.
helpviewer_keywords: ["ITCallInfo interface [TAPI 2.2]","SetCallInfoBuffer method","ITCallInfo.SetCallInfoBuffer","ITCallInfo::SetCallInfoBuffer","SetCallInfoBuffer","SetCallInfoBuffer method [TAPI 2.2]","SetCallInfoBuffer method [TAPI 2.2]","ITCallInfo interface","_tapi3_itcallinfo_setcallinfobuffer","tapi3.itcallinfo_setcallinfobuffer","tapi3if/ITCallInfo::SetCallInfoBuffer"]
old-location: tapi3\itcallinfo_setcallinfobuffer.htm
tech.root: tapi3
ms.assetid: fafe3c99-4584-43eb-b446-a9f2b9308097
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],SetCallInfoBuffer method, ITCallInfo.SetCallInfoBuffer, ITCallInfo::SetCallInfoBuffer, SetCallInfoBuffer, SetCallInfoBuffer method [TAPI 2.2], SetCallInfoBuffer method [TAPI 2.2],ITCallInfo interface, _tapi3_itcallinfo_setcallinfobuffer, tapi3.itcallinfo_setcallinfobuffer, tapi3if/ITCallInfo::SetCallInfoBuffer
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
 - ITCallInfo::SetCallInfoBuffer
 - tapi3if/ITCallInfo::SetCallInfoBuffer
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
 - ITCallInfo.SetCallInfoBuffer
---

# ITCallInfo::SetCallInfoBuffer


## -description

The 
<b>SetCallInfoBuffer</b> method sets call information items that require a buffer, such as user-user information. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer">ITCallInfo::put_CallInfoBuffer</a> method.

## -parameters

### -param CallInfoBuffer [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_buffer">CALLINFO_BUFFER</a> indicator of information type needed, such as CIB_USERUSERINFO.

### -param dwSize [in]

Size of <i>pCallInfoBuffer</i>.

### -param pCallInfoBuffer [in]

Pointer to call information buffer.

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
The <i>pCallInfoBuffer</i> parameter is not a valid pointer.

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



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer">get_CallInfoBuffer</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer">put_CallInfoBuffer</a>