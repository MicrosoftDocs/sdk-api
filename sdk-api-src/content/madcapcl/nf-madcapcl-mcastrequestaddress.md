---
UID: NF:madcapcl.McastRequestAddress
title: McastRequestAddress function (madcapcl.h)
description: The McastRequestAddress function requests one or more multicast addresses from a MADCAP server.
helpviewer_keywords: ["McastRequestAddress","McastRequestAddress function [MADCAP]","_mdhcp_mcastrequestaddress","madcap.mcastrequestaddress","madcapcl/McastRequestAddress"]
old-location: madcap\mcastrequestaddress.htm
tech.root: Madcap
ms.assetid: 856eb251-1909-41a1-8e4f-c081942280de
ms.date: 12/05/2018
ms.keywords: McastRequestAddress, McastRequestAddress function [MADCAP], _mdhcp_mcastrequestaddress, madcap.mcastrequestaddress, madcapcl/McastRequestAddress
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
 - McastRequestAddress
 - madcapcl/McastRequestAddress
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
 - McastRequestAddress
---

# McastRequestAddress function


## -description

The 
<b>McastRequestAddress</b> function requests one or more multicast addresses from a MADCAP server.

## -parameters

### -param AddrFamily [in]

Specifies the address family to be used in the request, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a> structure. Use AF_INET for IPv4 addresses and AF_INET6 for IPv6 addresses.

### -param pRequestID [in]

Pointer to a unique identifier for the request, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_client_uid">MCAST_CLIENT_UID</a> structure. Clients are responsible for ensuring that each request contains a unique identifier; unique identifiers can be obtained by calling the 
<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastgenuid">McastGenUID</a> function.

### -param pScopeCtx [in]

Pointer to the context of the scope from which the address is to be allocated, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_ctx">MCAST_SCOPE_CTX</a> structure. The scope context must be retrieved by calling the 
<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastenumeratescopes">McastEnumerateScopes</a> function prior to calling the 
<b>McastRequestAddress</b> function.

### -param pAddrRequest [in]

Pointer to the 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_request">MCAST_LEASE_REQUEST</a> structure containing multicast lease–request parameters.

### -param pAddrResponse [in, out]

Pointer to a buffer containing response parameters for the multicast address request, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_response">MCAST_LEASE_RESPONSE</a> structure. The caller is responsible for allocating sufficient buffer space for the <i>pAddrBuf</i> member of the 
<b>MCAST_LEASE_RESPONSE</b> structure to hold the requested number of addresses; the caller is also responsible for setting the pointer to that buffer.

## -returns

The 
<b>McastRequestAddress</b> function returns the status of the operation.

## -remarks

Before the 
<b>McastRequestAddress</b> function is called, the scope context must be retrieved by calling the 
<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastenumeratescopes">McastEnumerateScopes</a> function.

## -see-also

<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_client_uid">MCAST_CLIENT_UID</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_request">MCAST_LEASE_REQUEST</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_response">MCAST_LEASE_RESPONSE</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_ctx">MCAST_SCOPE_CTX</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_entry">MCAST_SCOPE_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapicleanup">McastApiCleanup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapistartup">McastApiStartup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastenumeratescopes">McastEnumerateScopes</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastgenuid">McastGenUID</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastreleaseaddress">McastReleaseAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrenewaddress">McastRenewAddress</a>