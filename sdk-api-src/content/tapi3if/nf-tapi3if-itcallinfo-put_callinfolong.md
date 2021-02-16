---
UID: NF:tapi3if.ITCallInfo.put_CallInfoLong
title: ITCallInfo::put_CallInfoLong (tapi3if.h)
description: The put_CallInfoLong method sets call information items described by a long, such as the bearer mode.
helpviewer_keywords: ["ITCallInfo interface [TAPI 2.2]","put_CallInfoLong method","ITCallInfo.put_CallInfoLong","ITCallInfo::put_CallInfoLong","_tapi3_itcallinfo_put_callinfolong","put_CallInfoLong","put_CallInfoLong method [TAPI 2.2]","put_CallInfoLong method [TAPI 2.2]","ITCallInfo interface","tapi3.itcallinfo_put_callinfolong","tapi3if/ITCallInfo::put_CallInfoLong"]
old-location: tapi3\itcallinfo_put_callinfolong.htm
tech.root: tapi3
ms.assetid: b5198b78-56f7-4964-970a-1068f2db4743
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],put_CallInfoLong method, ITCallInfo.put_CallInfoLong, ITCallInfo::put_CallInfoLong, _tapi3_itcallinfo_put_callinfolong, put_CallInfoLong, put_CallInfoLong method [TAPI 2.2], put_CallInfoLong method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_put_callinfolong, tapi3if/ITCallInfo::put_CallInfoLong
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
 - ITCallInfo::put_CallInfoLong
 - tapi3if/ITCallInfo::put_CallInfoLong
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
 - ITCallInfo.put_CallInfoLong
---

# ITCallInfo::put_CallInfoLong


## -description

The 
<b>put_CallInfoLong</b> method sets call information items described by a long, such as the bearer mode.

## -parameters

### -param CallInfoLong [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callinfo_long">CALLINFO_LONG</a> indicator of information type needed, such as CIL_BEARERMODE.

### -param lCallInfoLongVal [in]

Pointer to new value.

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



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong">get_CallInfoLong</a>