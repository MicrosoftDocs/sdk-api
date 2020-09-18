---
UID: NF:rend.ITRendezvous.EnumerateDefaultDirectories
title: ITRendezvous::EnumerateDefaultDirectories (rend.h)
description: The EnumerateDefaultDirectories method enumerates all configured default directories. This method is similar to get_DefaultDirectories but is designed for C/C++.
helpviewer_keywords: ["EnumerateDefaultDirectories","EnumerateDefaultDirectories method [TAPI 2.2]","EnumerateDefaultDirectories method [TAPI 2.2]","ITRendezvous interface","ITRendezvous interface [TAPI 2.2]","EnumerateDefaultDirectories method","ITRendezvous.EnumerateDefaultDirectories","ITRendezvous::EnumerateDefaultDirectories","_tapi3_itrendezvous_enumeratedefaultdirectories","rend/ITRendezvous::EnumerateDefaultDirectories","tapi3.itrendezvous_enumeratedefaultdirectories"]
old-location: tapi3\itrendezvous_enumeratedefaultdirectories.htm
tech.root: tapi3
ms.assetid: fe89a370-32ed-4519-bb98-9d9ea7615eb7
ms.date: 12/05/2018
ms.keywords: EnumerateDefaultDirectories, EnumerateDefaultDirectories method [TAPI 2.2], EnumerateDefaultDirectories method [TAPI 2.2],ITRendezvous interface, ITRendezvous interface [TAPI 2.2],EnumerateDefaultDirectories method, ITRendezvous.EnumerateDefaultDirectories, ITRendezvous::EnumerateDefaultDirectories, _tapi3_itrendezvous_enumeratedefaultdirectories, rend/ITRendezvous::EnumerateDefaultDirectories, tapi3.itrendezvous_enumeratedefaultdirectories
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
 - ITRendezvous::EnumerateDefaultDirectories
 - rend/ITRendezvous::EnumerateDefaultDirectories
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
 - ITRendezvous.EnumerateDefaultDirectories
---

# ITRendezvous::EnumerateDefaultDirectories


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>EnumerateDefaultDirectories</b> method enumerates all configured default directories. This method is similar to 
<a href="/windows/desktop/api/rend/nf-rend-itrendezvous-get_defaultdirectories">get_DefaultDirectories</a> but is designed for C/C++.

## -parameters

### -param ppEnumDirectory [out]

Pointer to receive 
<a href="/windows/desktop/api/rend/nn-rend-ienumdirectory">IEnumDirectory</a> enumerator listing default directories.

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
Pointer is invalid.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/rend/nn-rend-ienumdirectory">IEnumDirectory</a> interface returned by <b>ITRendezvous::EnumerateDefaultDirectories</b>. The application must call <b>Release</b> on the 
<b>IEnumDirectory</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-ienumdirectory">IEnumDirectory</a>



<a href="/windows/desktop/api/rend/nn-rend-itrendezvous">ITRendezvous</a>