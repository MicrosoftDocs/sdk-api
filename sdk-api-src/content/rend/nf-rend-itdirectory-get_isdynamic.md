---
UID: NF:rend.ITDirectory.get_IsDynamic
title: ITDirectory::get_IsDynamic (rend.h)
description: The get_IsDynamic method gets an indicator of whether the object on the server needs to be refreshed.
helpviewer_keywords: ["ITDirectory interface [TAPI 2.2]","get_IsDynamic method","ITDirectory.get_IsDynamic","ITDirectory::get_IsDynamic","_tapi3_itdirectory_get_isdynamic","get_IsDynamic","get_IsDynamic method [TAPI 2.2]","get_IsDynamic method [TAPI 2.2]","ITDirectory interface","rend/ITDirectory::get_IsDynamic","tapi3.itdirectory_get_isdynamic"]
old-location: tapi3\itdirectory_get_isdynamic.htm
tech.root: tapi3
ms.assetid: 4260ad95-d684-44e4-877f-fcdbe4fe0fd7
ms.date: 12/05/2018
ms.keywords: ITDirectory interface [TAPI 2.2],get_IsDynamic method, ITDirectory.get_IsDynamic, ITDirectory::get_IsDynamic, _tapi3_itdirectory_get_isdynamic, get_IsDynamic, get_IsDynamic method [TAPI 2.2], get_IsDynamic method [TAPI 2.2],ITDirectory interface, rend/ITDirectory::get_IsDynamic, tapi3.itdirectory_get_isdynamic
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
 - ITDirectory::get_IsDynamic
 - rend/ITDirectory::get_IsDynamic
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
 - ITDirectory.get_IsDynamic
---

# ITDirectory::get_IsDynamic


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_IsDynamic</b> method gets an indicator of whether the object on the server needs to be refreshed.

## -parameters

### -param pfDynamic [out]

Pointer to a Boolean <b>VARIANT</b>; VARIANT_TRUE if server needs to be refreshed and VARIANT_FALSE if it does not.

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
The <i>pfDynamic</i> parameter is not a valid pointer.

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