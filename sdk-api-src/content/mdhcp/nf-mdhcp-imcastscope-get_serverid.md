---
UID: NF:mdhcp.IMcastScope.get_ServerID
title: IMcastScope::get_ServerID (mdhcp.h)
description: The get_ServerID method obtains the server ID associated with this scope.
helpviewer_keywords: ["IMcastScope interface [TAPI 2.2]","get_ServerID method","IMcastScope.get_ServerID","IMcastScope::get_ServerID","_tapi3_imcastscope_get_serverid","get_ServerID","get_ServerID method [TAPI 2.2]","get_ServerID method [TAPI 2.2]","IMcastScope interface","mdhcp/IMcastScope::get_ServerID","tapi3.imcastscope_get_serverid"]
old-location: tapi3\imcastscope_get_serverid.htm
tech.root: tapi3
ms.assetid: 80c0ecca-647f-4e5e-92d6-fc95368715ad
ms.date: 12/05/2018
ms.keywords: IMcastScope interface [TAPI 2.2],get_ServerID method, IMcastScope.get_ServerID, IMcastScope::get_ServerID, _tapi3_imcastscope_get_serverid, get_ServerID, get_ServerID method [TAPI 2.2], get_ServerID method [TAPI 2.2],IMcastScope interface, mdhcp/IMcastScope::get_ServerID, tapi3.imcastscope_get_serverid
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
 - IMcastScope::get_ServerID
 - mdhcp/IMcastScope::get_ServerID
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
 - IMcastScope.get_ServerID
---

# IMcastScope::get_ServerID


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_ServerID</b> method obtains the server ID associated with this scope. The scope ID and server ID are needed to select this scope in subsequent calls to 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress">IMcastAddressAllocation::RequestAddress</a>, 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-renewaddress">IMcastAddressAllocation::RenewAddress</a>, or 
<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastaddressallocation-releaseaddress">IMcastAddressAllocation::ReleaseAddress</a>.

## -parameters

### -param pID [out]

Pointer to a <b>LONG</b> that will receive the server ID of this scope, which is the ID that was assigned to the multicast address allocation server that published this scope at the time that the server was configured.

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



<a href="/windows/desktop/api/mdhcp/nf-mdhcp-imcastscope-get_scopeid">IMcastScope::get_ScopeID</a>