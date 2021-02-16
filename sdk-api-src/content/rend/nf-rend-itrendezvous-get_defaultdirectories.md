---
UID: NF:rend.ITRendezvous.get_DefaultDirectories
title: ITRendezvous::get_DefaultDirectories (rend.h)
description: The get_DefaultDirectories method enumerates all configured default directories. This method is similar to EnumerateDefaultDirectories but is provided for use by Visual Basic and other scripting languages.
helpviewer_keywords: ["ITRendezvous interface [TAPI 2.2]","get_DefaultDirectories method","ITRendezvous.get_DefaultDirectories","ITRendezvous::get_DefaultDirectories","_tapi3_itrendezvous_get_defaultdirectories","get_DefaultDirectories","get_DefaultDirectories method [TAPI 2.2]","get_DefaultDirectories method [TAPI 2.2]","ITRendezvous interface","rend/ITRendezvous::get_DefaultDirectories","tapi3.itrendezvous_get_defaultdirectories"]
old-location: tapi3\itrendezvous_get_defaultdirectories.htm
tech.root: tapi3
ms.assetid: 3db02f17-6fb5-467b-91f6-dc501b5472cf
ms.date: 12/05/2018
ms.keywords: ITRendezvous interface [TAPI 2.2],get_DefaultDirectories method, ITRendezvous.get_DefaultDirectories, ITRendezvous::get_DefaultDirectories, _tapi3_itrendezvous_get_defaultdirectories, get_DefaultDirectories, get_DefaultDirectories method [TAPI 2.2], get_DefaultDirectories method [TAPI 2.2],ITRendezvous interface, rend/ITRendezvous::get_DefaultDirectories, tapi3.itrendezvous_get_defaultdirectories
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
 - ITRendezvous::get_DefaultDirectories
 - rend/ITRendezvous::get_DefaultDirectories
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
 - ITRendezvous.get_DefaultDirectories
---

# ITRendezvous::get_DefaultDirectories


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_DefaultDirectories</b> method enumerates all configured default directories. This method is similar to 
<a href="/windows/desktop/api/rend/nf-rend-itrendezvous-enumeratedefaultdirectories">EnumerateDefaultDirectories</a> but is provided for use by Visual Basic and other scripting languages.

## -parameters

### -param pVariant [out]

Pointer to a <b>VARIANT</b> that will receive an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a> interface pointers.

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
Insufficient memory exists to create a collection.

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
<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a> interface returned by <b>ITRendezvous::get_DefaultDirectories</b>. The application must call <b>Release</b> on the 
<b>ITDirectory</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>



<a href="/windows/desktop/api/rend/nn-rend-itrendezvous">ITRendezvous</a>