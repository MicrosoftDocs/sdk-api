---
UID: NF:mdhcp.IMcastLeaseInfo.get_TTL
title: IMcastLeaseInfo::get_TTL (mdhcp.h)
description: The get_TTL method obtains the time to live (TTL) value associated with this lease.
helpviewer_keywords: ["IMcastLeaseInfo interface [TAPI 2.2]","get_TTL method","IMcastLeaseInfo.get_TTL","IMcastLeaseInfo::get_TTL","_tapi3_imcastleaseinfo_get_ttl","get_TTL","get_TTL method [TAPI 2.2]","get_TTL method [TAPI 2.2]","IMcastLeaseInfo interface","mdhcp/IMcastLeaseInfo::get_TTL","tapi3.imcastleaseinfo_get_ttl"]
old-location: tapi3\imcastleaseinfo_get_ttl.htm
tech.root: tapi3
ms.assetid: 393b9d6c-430c-42f8-88fa-4bf5c9c04c1f
ms.date: 12/05/2018
ms.keywords: IMcastLeaseInfo interface [TAPI 2.2],get_TTL method, IMcastLeaseInfo.get_TTL, IMcastLeaseInfo::get_TTL, _tapi3_imcastleaseinfo_get_ttl, get_TTL, get_TTL method [TAPI 2.2], get_TTL method [TAPI 2.2],IMcastLeaseInfo interface, mdhcp/IMcastLeaseInfo::get_TTL, tapi3.imcastleaseinfo_get_ttl
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
 - IMcastLeaseInfo::get_TTL
 - mdhcp/IMcastLeaseInfo::get_TTL
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
 - IMcastLeaseInfo.get_TTL
---

# IMcastLeaseInfo::get_TTL


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The <b>get_TTL</b> method obtains the <a href="/windows/win32/tapi/t-tapgloss">time to live</a> (TTL) value associated with this lease.

## -parameters

### -param pTTL [out]

Pointer to a <b>LONG</b> that will receive the TTL value associated with this lease.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The caller passed in an invalid pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There is no TTL associated with this lease.

</td>
</tr>
</table>

## -remarks

The TTL is more or less significant in the implementation of multicast routing. Generally, the higher the TTL value, the "larger" or more inclusive the multicast scope. Most applications need not address the TTL.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastleaseinfo">IMcastLeaseInfo</a>