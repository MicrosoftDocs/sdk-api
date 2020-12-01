---
UID: NF:mdhcp.IMcastAddressAllocation.get_Scopes
title: IMcastAddressAllocation::get_Scopes (mdhcp.h)
description: The get_Scopes method creates a collection of IMcast scopes available. This method is similar to EnumerateScopes, but is used by scripting languages such as Visual Basic.
helpviewer_keywords: ["IMcastAddressAllocation interface [TAPI 2.2]","get_Scopes method","IMcastAddressAllocation.get_Scopes","IMcastAddressAllocation::get_Scopes","_tapi3_imcastaddressallocation_get_scopes","get_Scopes","get_Scopes method [TAPI 2.2]","get_Scopes method [TAPI 2.2]","IMcastAddressAllocation interface","mdhcp/IMcastAddressAllocation::get_Scopes","tapi3.imcastaddressallocation_get_scopes"]
old-location: tapi3\imcastaddressallocation_get_scopes.htm
tech.root: tapi3
ms.assetid: 4fe824fa-2fcb-4f6b-b3de-15dcfc79575c
ms.date: 12/05/2018
ms.keywords: IMcastAddressAllocation interface [TAPI 2.2],get_Scopes method, IMcastAddressAllocation.get_Scopes, IMcastAddressAllocation::get_Scopes, _tapi3_imcastaddressallocation_get_scopes, get_Scopes, get_Scopes method [TAPI 2.2], get_Scopes method [TAPI 2.2],IMcastAddressAllocation interface, mdhcp/IMcastAddressAllocation::get_Scopes, tapi3.imcastaddressallocation_get_scopes
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
 - IMcastAddressAllocation::get_Scopes
 - mdhcp/IMcastAddressAllocation::get_Scopes
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
 - IMcastAddressAllocation.get_Scopes
---

# IMcastAddressAllocation::get_Scopes


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_Scopes</b> method creates a collection of IMcast scopes available. This method is similar to 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes">EnumerateScopes</a>, but is used by scripting languages such as Visual Basic.

## -parameters

### -param pVariant [out]

Pointer to a <b>VARIANT</b> receiving an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a> interface pointers.

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
<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a> interface returned by <b>IMcastAddressAllocation::get_Scopes</b>. The application must call <b>Release</b> on the 
<b>IMcastScope</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastaddressallocation">IMcastAddressAllocation</a>



<a href="/windows/desktop/api/mdhcp/nn-mdhcp-imcastscope">IMcastScope</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>