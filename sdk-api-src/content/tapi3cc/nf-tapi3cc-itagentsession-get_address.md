---
UID: NF:tapi3cc.ITAgentSession.get_Address
title: ITAgentSession::get_Address (tapi3cc.h)
description: The ITAgentSession::get_Address method (tapi3cc.h) gets a pointer to the ITAddress interface associated with this session.
helpviewer_keywords: ["ITAgentSession interface [TAPI 2.2]","get_Address method","ITAgentSession.get_Address","ITAgentSession::get_Address","_tapi3_itagentsession_get_address","get_Address","get_Address method [TAPI 2.2]","get_Address method [TAPI 2.2]","ITAgentSession interface","tapi3.itagentsession_get_address","tapi3cc/ITAgentSession::get_Address"]
old-location: tapi3\itagentsession_get_address.htm
tech.root: tapi3
ms.assetid: addd088d-5bca-4865-8cae-3c013554dafd
ms.date: 08/10/2022
ms.keywords: ITAgentSession interface [TAPI 2.2],get_Address method, ITAgentSession.get_Address, ITAgentSession::get_Address, _tapi3_itagentsession_get_address, get_Address, get_Address method [TAPI 2.2], get_Address method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_address, tapi3cc/ITAgentSession::get_Address
req.header: tapi3cc.h
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
 - ITAgentSession::get_Address
 - tapi3cc/ITAgentSession::get_Address
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
 - ITAgentSession.get_Address
---

# ITAgentSession::get_Address


## -description

The 
<b>get_Address</b> method gets a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface associated with this session.

## -parameters

### -param ppAddress [out]

Pointer for 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>.

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
The <i>ppAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface returned by <b>ITAgentSession::get_Address</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a>
