---
UID: NF:tapi3.ITAgentSession.get_ACDGroup
title: ITAgentSession::get_ACDGroup (tapi3.h)
description: The get_ACDGroup method (tapi3.h) gets the ACD group associated with this session.
helpviewer_keywords: ["ITAgentSession interface [TAPI 2.2]","get_ACDGroup method","ITAgentSession.get_ACDGroup","ITAgentSession::get_ACDGroup","_tapi3_itagentsession_get_acdgroup","get_ACDGroup","get_ACDGroup method [TAPI 2.2]","get_ACDGroup method [TAPI 2.2]","ITAgentSession interface","tapi3.itagentsession_get_acdgroup","tapi3cc/ITAgentSession::get_ACDGroup"]
old-location: tapi3\itagentsession_get_acdgroup.htm
tech.root: tapi3
ms.assetid: ec80092d-ceff-432c-ba0a-695718b890af
ms.date: 08/09/2022
ms.keywords: ITAgentSession interface [TAPI 2.2],get_ACDGroup method, ITAgentSession.get_ACDGroup, ITAgentSession::get_ACDGroup, _tapi3_itagentsession_get_acdgroup, get_ACDGroup, get_ACDGroup method [TAPI 2.2], get_ACDGroup method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_acdgroup, tapi3cc/ITAgentSession::get_ACDGroup
req.header: tapi3.h
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
 - ITAgentSession::get_ACDGroup
 - tapi3/ITAgentSession::get_ACDGroup
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
 - ITAgentSession.get_ACDGroup
---

# ITAgentSession::get_ACDGroup


## -description

The 
<b>get_ACDGroup</b> method gets the ACD group associated with this session.

## -parameters

### -param ppACDGroup [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a> interface.

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
The <i>ppACDGroup</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LINEERR_</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentsessioninfo">lineGetAgentSessionInfo</a> for error codes returned from this TAPI 2.1 function.

</td>
</tr>
</table>

## -remarks

This method wraps the TAPI 2.1 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentsessioninfo">lineGetAgentSessionInfo</a> function.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a> interface returned by <b>ITAgentSession::get_ACDGroup</b>. The application must call <b>Release</b> on the 
<b>ITACDGroup</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentsessioninfo">lineGetAgentSessionInfo</a>
