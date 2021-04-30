---
UID: NF:rend.ITDirectoryObjectConference.get_IsEncrypted
title: ITDirectoryObjectConference::get_IsEncrypted (rend.h)
description: The get_IsEncrypted method gets whether the conference is encrypted.
helpviewer_keywords: ["ITDirectoryObjectConference interface [TAPI 2.2]","get_IsEncrypted method","ITDirectoryObjectConference.get_IsEncrypted","ITDirectoryObjectConference::get_IsEncrypted","_tapi3_itdirectoryobjectconference_get_isencrypted","get_IsEncrypted","get_IsEncrypted method [TAPI 2.2]","get_IsEncrypted method [TAPI 2.2]","ITDirectoryObjectConference interface","rend/ITDirectoryObjectConference::get_IsEncrypted","tapi3.itdirectoryobjectconference_get_isencrypted"]
old-location: tapi3\itdirectoryobjectconference_get_isencrypted.htm
tech.root: tapi3
ms.assetid: a3228efa-2501-44ec-ba85-0e3b7c00b483
ms.date: 12/05/2018
ms.keywords: ITDirectoryObjectConference interface [TAPI 2.2],get_IsEncrypted method, ITDirectoryObjectConference.get_IsEncrypted, ITDirectoryObjectConference::get_IsEncrypted, _tapi3_itdirectoryobjectconference_get_isencrypted, get_IsEncrypted, get_IsEncrypted method [TAPI 2.2], get_IsEncrypted method [TAPI 2.2],ITDirectoryObjectConference interface, rend/ITDirectoryObjectConference::get_IsEncrypted, tapi3.itdirectoryobjectconference_get_isencrypted
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
 - ITDirectoryObjectConference::get_IsEncrypted
 - rend/ITDirectoryObjectConference::get_IsEncrypted
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
 - ITDirectoryObjectConference.get_IsEncrypted
---

# ITDirectoryObjectConference::get_IsEncrypted


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_IsEncrypted</b> method gets whether the conference is encrypted.

## -parameters

### -param pfEncrypted [out]

Pointer to whether the conference is encrypted.

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
The <i>pfEncrypted</i> parameter is not a valid pointer.

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

<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_isencrypted">ITDirectoryObjectConference::put_IsEncrypted</a>