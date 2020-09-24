---
UID: NF:tapi3if.ITCallInfo.get_CallInfoLong
title: ITCallInfo::get_CallInfoLong (tapi3if.h)
description: The get_CallInfoLong method gets call information items described by a long, such as the bearer mode.
helpviewer_keywords: ["ITCallInfo interface [TAPI 2.2]","get_CallInfoLong method","ITCallInfo.get_CallInfoLong","ITCallInfo::get_CallInfoLong","_tapi3_itcallinfo_get_callinfolong","get_CallInfoLong","get_CallInfoLong method [TAPI 2.2]","get_CallInfoLong method [TAPI 2.2]","ITCallInfo interface","tapi3.itcallinfo_get_callinfolong","tapi3if/ITCallInfo::get_CallInfoLong"]
old-location: tapi3\itcallinfo_get_callinfolong.htm
tech.root: tapi3
ms.assetid: 0c00e672-7bad-4a44-a76a-efd222f763d7
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_CallInfoLong method, ITCallInfo.get_CallInfoLong, ITCallInfo::get_CallInfoLong, _tapi3_itcallinfo_get_callinfolong, get_CallInfoLong, get_CallInfoLong method [TAPI 2.2], get_CallInfoLong method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_callinfolong, tapi3if/ITCallInfo::get_CallInfoLong
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
 - ITCallInfo::get_CallInfoLong
 - tapi3if/ITCallInfo::get_CallInfoLong
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
 - ITCallInfo.get_CallInfoLong
---

# ITCallInfo::get_CallInfoLong


## -description

The 
<b>get_CallInfoLong</b> method gets call information items described by a long, such as the bearer mode.

## -parameters

### -param CallInfoLong [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_long">CALLINFO_LONG</a> indicator of information type needed, such as CIL_BEARERMODE.

### -param plCallInfoLongVal [out]

Pointer to value returned.

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
The <i>plCallInfoLongVal</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>CallInfoLong</i> parameter is not a valid value.

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

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_long">CALLINFO_LONG</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong">put_CallInfoLong</a>