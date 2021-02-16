---
UID: NF:tapi3if.ITCallInfo.get_CallHub
title: ITCallInfo::get_CallHub (tapi3if.h)
description: The get_CallHub method gets a pointer to the ITCallHub interface of the CallHub object.
helpviewer_keywords: ["ITCallInfo interface [TAPI 2.2]","get_CallHub method","ITCallInfo.get_CallHub","ITCallInfo::get_CallHub","_tapi3_itcallinfo_get_callhub","get_CallHub","get_CallHub method [TAPI 2.2]","get_CallHub method [TAPI 2.2]","ITCallInfo interface","tapi3.itcallinfo_get_callhub","tapi3if/ITCallInfo::get_CallHub"]
old-location: tapi3\itcallinfo_get_callhub.htm
tech.root: tapi3
ms.assetid: ae7d74f7-c69b-45d1-a049-59e581856f27
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_CallHub method, ITCallInfo.get_CallHub, ITCallInfo::get_CallHub, _tapi3_itcallinfo_get_callhub, get_CallHub, get_CallHub method [TAPI 2.2], get_CallHub method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_callhub, tapi3if/ITCallInfo::get_CallHub
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
 - ITCallInfo::get_CallHub
 - tapi3if/ITCallInfo::get_CallHub
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
 - ITCallInfo.get_CallHub
---

# ITCallInfo::get_CallHub


## -description

The 
<b>get_CallHub</b> method gets a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a> interface of the 
<a href="/windows/desktop/Tapi/callhub-object">CallHub object</a>.

## -parameters

### -param ppCallHub [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a> interface of the CallHub object.

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
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Call hub not yet available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCallHub</i> parameter is not a valid pointer.

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

On some service providers, the call hub is not available until after the call is made.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a> interface returned by <b>ITCallInfo::get_CallHub</b>. The application must call <b>Release</b> on the 
<b>ITCallHub</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/Tapi/callhub-object">CallHub object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>