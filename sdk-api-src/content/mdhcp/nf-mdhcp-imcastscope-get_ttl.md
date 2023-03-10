---
UID: NF:mdhcp.IMcastScope.get_TTL
title: IMcastScope::get_TTL (mdhcp.h)
description: The get_TTL method obtains the time to live value for the multicast scope.
helpviewer_keywords: ["IMcastScope interface [TAPI 2.2]","get_TTL method","IMcastScope.get_TTL","IMcastScope::get_TTL","_tapi3_imcastscope_get_ttl","get_TTL","get_TTL method [TAPI 2.2]","get_TTL method [TAPI 2.2]","IMcastScope interface","mdhcp/IMcastScope::get_TTL","tapi3.imcastscope_get_ttl"]
old-location: tapi3\imcastscope_get_ttl.htm
tech.root: tapi3
ms.assetid: 68e402e5-87ae-49fd-9149-8eb79a0a8aee
ms.date: 12/05/2018
ms.keywords: IMcastScope interface [TAPI 2.2],get_TTL method, IMcastScope.get_TTL, IMcastScope::get_TTL, _tapi3_imcastscope_get_ttl, get_TTL, get_TTL method [TAPI 2.2], get_TTL method [TAPI 2.2],IMcastScope interface, mdhcp/IMcastScope::get_TTL, tapi3.imcastscope_get_ttl
req.header: mdhcp.h
req.include-header: 
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
req.dll: Mdhcp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMcastScope::get_TTL
 - mdhcp/IMcastScope::get_TTL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mdhcp.dll
api_name:
 - IMcastScope.get_TTL
---

# IMcastScope::get_TTL


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_TTL</b> method obtains the time to live value for the multicast scope.

## -parameters

### -param pTTL [out]

Pointer to a time to live value for multicast scope.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The caller passed in an invalid pointer argument.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a>