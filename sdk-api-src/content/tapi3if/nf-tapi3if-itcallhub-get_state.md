---
UID: NF:tapi3if.ITCallHub.get_State
title: ITCallHub::get_State (tapi3if.h)
description: The get_State method gets the current state of the CallHub.
helpviewer_keywords: ["ITCallHub interface [TAPI 2.2]","get_State method","ITCallHub.get_State","ITCallHub::get_State","_tapi3_itcallhub_get_state","get_State","get_State method [TAPI 2.2]","get_State method [TAPI 2.2]","ITCallHub interface","tapi3.itcallhub_get_state","tapi3if/ITCallHub::get_State"]
old-location: tapi3\itcallhub_get_state.htm
tech.root: tapi3
ms.assetid: 0ca4bbad-6822-4a8b-8df4-da6e630752f0
ms.date: 12/05/2018
ms.keywords: ITCallHub interface [TAPI 2.2],get_State method, ITCallHub.get_State, ITCallHub::get_State, _tapi3_itcallhub_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITCallHub interface, tapi3.itcallhub_get_state, tapi3if/ITCallHub::get_State
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
 - ITCallHub::get_State
 - tapi3if/ITCallHub::get_State
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
 - ITCallHub.get_State
---

# ITCallHub::get_State


## -description

The 
<b>get_State</b> method gets the current state of the CallHub.

## -parameters

### -param pState [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callhub_state">CALLHUB_STATE</a> indicator of state.

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
The <i>pState</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callhub_state">CALLHUB_STATE</a>



<a href="/windows/desktop/Tapi/callhub-object">CallHub Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a>