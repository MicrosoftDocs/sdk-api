---
UID: NF:rend.ITDirectory.get_DefaultObjectTTL
title: ITDirectory::get_DefaultObjectTTL (rend.h)
description: The get_DefaultObjectTTL method gets the default time to live (TTL) value, in seconds, for objects created. Only applies to dynamic servers.
helpviewer_keywords: ["ITDirectory interface [TAPI 2.2]","get_DefaultObjectTTL method","ITDirectory.get_DefaultObjectTTL","ITDirectory::get_DefaultObjectTTL","_tapi3_itdirectory_get_defaultobjectttl","get_DefaultObjectTTL","get_DefaultObjectTTL method [TAPI 2.2]","get_DefaultObjectTTL method [TAPI 2.2]","ITDirectory interface","rend/ITDirectory::get_DefaultObjectTTL","tapi3.itdirectory_get_defaultobjectttl"]
old-location: tapi3\itdirectory_get_defaultobjectttl.htm
tech.root: tapi3
ms.assetid: f0a24ad9-0020-4f62-a0f2-071b9d251f79
ms.date: 12/05/2018
ms.keywords: ITDirectory interface [TAPI 2.2],get_DefaultObjectTTL method, ITDirectory.get_DefaultObjectTTL, ITDirectory::get_DefaultObjectTTL, _tapi3_itdirectory_get_defaultobjectttl, get_DefaultObjectTTL, get_DefaultObjectTTL method [TAPI 2.2], get_DefaultObjectTTL method [TAPI 2.2],ITDirectory interface, rend/ITDirectory::get_DefaultObjectTTL, tapi3.itdirectory_get_defaultobjectttl
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITDirectory::get_DefaultObjectTTL
 - rend/ITDirectory::get_DefaultObjectTTL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectory.get_DefaultObjectTTL
---

# ITDirectory::get_DefaultObjectTTL


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_DefaultObjectTTL</b> method gets the default 
<a href="/windows/win32/tapi/t-tapgloss">time to live</a> (TTL) value, in seconds, for objects created. Only applies to dynamic servers.

## -parameters

### -param pTTL [out]

Pointer to TTL value, in seconds.

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
The <i>pTTL</i> parameter is not a valid pointer.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not yet implemented.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectory-put_defaultobjectttl">ITDirectory::put_DefaultObjectTTL</a>