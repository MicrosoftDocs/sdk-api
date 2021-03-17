---
UID: NF:madcapcl.McastEnumerateScopes
title: McastEnumerateScopes function (madcapcl.h)
description: The McastEnumerateScopes function enumerates multicast scopes available on the network.
helpviewer_keywords: ["McastEnumerateScopes","McastEnumerateScopes function [MADCAP]","_mdhcp_mcastenumeratescopes","madcap.mcastenumeratescopes","madcapcl/McastEnumerateScopes"]
old-location: madcap\mcastenumeratescopes.htm
tech.root: Madcap
ms.assetid: df33d766-d420-4069-8b94-86f5e4e91c1d
ms.date: 12/05/2018
ms.keywords: McastEnumerateScopes, McastEnumerateScopes function [MADCAP], _mdhcp_mcastenumeratescopes, madcap.mcastenumeratescopes, madcapcl/McastEnumerateScopes
req.header: madcapcl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dhcpcsvc.lib
req.dll: Dhcpcsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - McastEnumerateScopes
 - madcapcl/McastEnumerateScopes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpcsvc.dll
api_name:
 - McastEnumerateScopes
---

# McastEnumerateScopes function


## -description

The 
<b>McastEnumerateScopes</b> function enumerates multicast scopes available on the network.

## -parameters

### -param AddrFamily [in]

Specifies the address family to be used in enumeration, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a> structure. Use AF_INET for IPv4 addresses and AF_INET6 for IPv6 addresses.

### -param ReQuery [in]

Enables a caller to query a list again. Set this parameter to <b>TRUE</b> if the list is to be queried more than once. Otherwise, set it to <b>FALSE</b>.

### -param pScopeList [in, out]

Pointer to a buffer used for storing scope list information, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_entry">MCAST_SCOPE_ENTRY</a> structure. The return value of <i>pScopeList</i> depends on its input value, and on the value of the buffer to which it points: 




If <i>pScopeList</i> is a valid pointer on input, the scope list is returned.

If <i>pScopeList</i> is <b>NULL</b> on input, the length of the buffer required to hold the scope list is returned.

If the buffer pointed to in <i>pScopeList</i> is <b>NULL</b> on input, 
<b>McastEnumerateScopes</b> forces a repeat querying of scope lists from MCAST servers.

To determine the size of buffer required to hold scope list data, set <i>pScopeList</i> to <b>NULL</b> and <i>pScopeLen</i> to a non-<b>NULL</b> value. The 
<b>McastEnumerateScopes</b> function will then return ERROR_SUCCESS and store the size of the scope list data, in bytes, in <i>pScopeLen</i>.

### -param pScopeLen [in, out]

Pointer to a value used to communicate the size of data or buffer space in <i>pScopeList</i>. On input, <i>pScopeLen</i> points to the size, in bytes, of the buffer pointed to by <i>pScopeList</i>. On return, <i>pScopeLen</i> points to the size of the data copied to <i>pScopeList</i>. 




The <i>pScopeLen</i> parameter cannot be <b>NULL</b>. If the buffer pointed to by <i>pScopeList</i> is not large enough to hold the scope list data, 
<b>McastEnumerateScopes</b> returns ERROR_MORE_DATA and stores the required buffer size, in bytes, in <i>pScopeLen</i>.

To determine the size of buffer required to hold scope list data, set <i>pScopeList</i> to <b>NULL</b> and <i>pScopeLen</i> to a non-<b>NULL</b> value. The 
<b>McastEnumerateScopes</b> function will then return ERROR_SUCCESS and store the size of the scope list data, in bytes, in <i>pScopeLen</i>.

### -param pScopeCount [out]

Pointer to the number of scopes returned in <i>pScopeList</i>.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.

If the buffer pointed to by <i>pScopeList</i> is too small to hold the scope list, the 
<b>McastEnumerateScopes</b> function returns ERROR_MORE_DATA, and stores the required buffer size, in bytes, in <i>pScopeLen</i>.

If the 
<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapistartup">McastApiStartup</a> function has not been called (it must be called before any other MADCAP client functions may be called), the 
<b>McastEnumerateScopes</b> function returns ERROR_NOT_READY.

## -remarks

The 
<b>McastEnumerateScopes</b> function queries multicast scopes for each network interface, and the interface on which the scope is retrieved is returned as part of the <i>pScopeList</i> parameter. Therefore, on multihomed computers it is possible that some scopes will get listed multiple times, once for each interface.

## -see-also

<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_client_uid">MCAST_CLIENT_UID</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_request">MCAST_LEASE_REQUEST</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_response">MCAST_LEASE_RESPONSE</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_ctx">MCAST_SCOPE_CTX</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_entry">MCAST_SCOPE_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapicleanup">McastApiCleanup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapistartup">McastApiStartup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastgenuid">McastGenUID</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastreleaseaddress">McastReleaseAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrenewaddress">McastRenewAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>