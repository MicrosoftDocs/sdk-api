---
UID: NF:mdhcp.IMcastAddressAllocation.EnumerateScopes
title: IMcastAddressAllocation::EnumerateScopes (mdhcp.h)
description: The EnumerateScopes method creates an enumeration of multicast scopes available. This method is primarily for C++ programmers. Visual Basic and other scripting languages use get_Scopes instead.
helpviewer_keywords: ["EnumerateScopes","EnumerateScopes method [TAPI 2.2]","EnumerateScopes method [TAPI 2.2]","IMcastAddressAllocation interface","IMcastAddressAllocation interface [TAPI 2.2]","EnumerateScopes method","IMcastAddressAllocation.EnumerateScopes","IMcastAddressAllocation::EnumerateScopes","_tapi3_imcastaddressallocation_enumeratescopes","mdhcp/IMcastAddressAllocation::EnumerateScopes","tapi3.imcastaddressallocation_enumeratescopes"]
old-location: tapi3\imcastaddressallocation_enumeratescopes.htm
tech.root: tapi3
ms.assetid: 1845f5f9-be0e-4609-89d8-1a0ed194dd68
ms.date: 12/05/2018
ms.keywords: EnumerateScopes, EnumerateScopes method [TAPI 2.2], EnumerateScopes method [TAPI 2.2],IMcastAddressAllocation interface, IMcastAddressAllocation interface [TAPI 2.2],EnumerateScopes method, IMcastAddressAllocation.EnumerateScopes, IMcastAddressAllocation::EnumerateScopes, _tapi3_imcastaddressallocation_enumeratescopes, mdhcp/IMcastAddressAllocation::EnumerateScopes, tapi3.imcastaddressallocation_enumeratescopes
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
 - IMcastAddressAllocation::EnumerateScopes
 - mdhcp/IMcastAddressAllocation::EnumerateScopes
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
 - IMcastAddressAllocation.EnumerateScopes
---

# IMcastAddressAllocation::EnumerateScopes


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>EnumerateScopes</b> method creates an enumeration of multicast scopes available. This method is primarily for C++ programmers. Visual Basic and other scripting languages use 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-get_scopes">get_Scopes</a> instead.

## -parameters

### -param ppEnumMcastScope [out]

Returns a pointer to a new 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-ienummcastscope">IEnumMcastScope</a> object.

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
There are no scopes available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory exists to create the required objects.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-ienummcastscope">IEnumMcastScope</a> interface returned by <b>IMcastAddressAllocation::EnumerateScopes</b>. The application must call <b>Release</b> on the 
<b>IEnumMcastScope</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastaddressallocation">IMcastAddressAllocation</a>