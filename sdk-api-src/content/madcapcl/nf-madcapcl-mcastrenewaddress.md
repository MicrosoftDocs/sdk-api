---
UID: NF:madcapcl.McastRenewAddress
title: McastRenewAddress function (madcapcl.h)
description: The McastRenewAddress function renews one or more multicast addresses from a MADCAP server.
helpviewer_keywords: ["McastRenewAddress","McastRenewAddress function [MADCAP]","_mdhcp_mcastrenewaddress","madcap.mcastrenewaddress","madcapcl/McastRenewAddress"]
old-location: madcap\mcastrenewaddress.htm
tech.root: Madcap
ms.assetid: d1d26edb-f372-4d6d-a6e2-a8eeafadedc0
ms.date: 12/05/2018
ms.keywords: McastRenewAddress, McastRenewAddress function [MADCAP], _mdhcp_mcastrenewaddress, madcap.mcastrenewaddress, madcapcl/McastRenewAddress
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
 - McastRenewAddress
 - madcapcl/McastRenewAddress
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
 - McastRenewAddress
---

# McastRenewAddress function


## -description

The 
<b>McastRenewAddress</b> function renews one or more multicast addresses from a MADCAP server.

## -parameters

### -param AddrFamily [in]

Designates the address family. Use AF_INET for Internet Protocol version 4 (IPv4), and AF_INET6 for Internet Protocol version 6 (IPv6).

### -param pRequestID [in]

Unique identifier used when the address or addresses were initially obtained.

### -param pRenewRequest [in]

Pointer to the 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_request">MCAST_LEASE_REQUEST</a> structure containing multicast renew–request parameters.

### -param pRenewResponse [in, out]

Pointer to a buffer containing response parameters for the multicast address–renew request, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_response">MCAST_LEASE_RESPONSE</a> structure. The caller is responsible for allocating sufficient buffer space for the <b>pAddrBuf</b> member of the 
<b>MCAST_LEASE_RESPONSE</b> structure to hold the requested number of addresses; the caller is also responsible for setting the pointer to that buffer.

## -returns

The 
<b>McastRenewAddress</b> function returns the status of the operation.

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



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>