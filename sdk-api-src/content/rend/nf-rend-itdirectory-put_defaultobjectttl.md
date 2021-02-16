---
UID: NF:rend.ITDirectory.put_DefaultObjectTTL
title: ITDirectory::put_DefaultObjectTTL (rend.h)
description: The put_DefaultObjectTTL method sets the default time to live (TTL) value, in seconds, for objects created. Only applies to dynamic servers. The minimum value is 300 seconds.
helpviewer_keywords: ["ITDirectory interface [TAPI 2.2]","put_DefaultObjectTTL method","ITDirectory.put_DefaultObjectTTL","ITDirectory::put_DefaultObjectTTL","_tapi3_itdirectory_put_defaultobjectttl","put_DefaultObjectTTL","put_DefaultObjectTTL method [TAPI 2.2]","put_DefaultObjectTTL method [TAPI 2.2]","ITDirectory interface","rend/ITDirectory::put_DefaultObjectTTL","tapi3.itdirectory_put_defaultobjectttl"]
old-location: tapi3\itdirectory_put_defaultobjectttl.htm
tech.root: tapi3
ms.assetid: aecadd26-648e-43ce-8331-ef4af24567ed
ms.date: 12/05/2018
ms.keywords: ITDirectory interface [TAPI 2.2],put_DefaultObjectTTL method, ITDirectory.put_DefaultObjectTTL, ITDirectory::put_DefaultObjectTTL, _tapi3_itdirectory_put_defaultobjectttl, put_DefaultObjectTTL, put_DefaultObjectTTL method [TAPI 2.2], put_DefaultObjectTTL method [TAPI 2.2],ITDirectory interface, rend/ITDirectory::put_DefaultObjectTTL, tapi3.itdirectory_put_defaultobjectttl
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
 - ITDirectory::put_DefaultObjectTTL
 - rend/ITDirectory::put_DefaultObjectTTL
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
 - ITDirectory.put_DefaultObjectTTL
---

# ITDirectory::put_DefaultObjectTTL


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>put_DefaultObjectTTL</b> method sets the default 
<a href="/windows/win32/tapi/t-tapgloss">time to live</a> (TTL) value, in seconds, for objects created. Only applies to dynamic servers. The minimum value is 300 seconds.

## -parameters

### -param TTL [in]

TTL value, in seconds.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>TTL</i> parameter is not valid.

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



<a href="/windows/desktop/api/rend/nf-rend-itdirectory-get_defaultobjectttl">ITDirectory::get_DefaultObjectTTL</a>