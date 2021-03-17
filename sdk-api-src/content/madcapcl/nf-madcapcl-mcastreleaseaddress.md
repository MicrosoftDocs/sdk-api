---
UID: NF:madcapcl.McastReleaseAddress
title: McastReleaseAddress function (madcapcl.h)
description: The McastReleaseAddress function releases leased multicast addresses from the MCAST server.
helpviewer_keywords: ["McastReleaseAddress","McastReleaseAddress function [MADCAP]","_mdhcp_mcastreleaseaddress","madcap.mcastreleaseaddress","madcapcl/McastReleaseAddress"]
old-location: madcap\mcastreleaseaddress.htm
tech.root: Madcap
ms.assetid: 6cb87e3b-0d2e-46f8-8ccf-6309c8fb888c
ms.date: 12/05/2018
ms.keywords: McastReleaseAddress, McastReleaseAddress function [MADCAP], _mdhcp_mcastreleaseaddress, madcap.mcastreleaseaddress, madcapcl/McastReleaseAddress
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
 - McastReleaseAddress
 - madcapcl/McastReleaseAddress
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
 - McastReleaseAddress
---

# McastReleaseAddress function


## -description

The 
<b>McastReleaseAddress</b> function releases leased multicast addresses from the MCAST server.

## -parameters

### -param AddrFamily [in]

Designates the address family. Use AF_INET for Internet Protocol version 4 (IPv4), and AF_INET6 for Internet Protocol version 6 (IPv6).

### -param pRequestID [in]

Unique identifier used when the address or addresses were initially obtained.

### -param pReleaseRequest [in]

Pointer to the 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_request">MCAST_LEASE_REQUEST</a> structure containing multicast parameters associated with the release request.

## -returns

The 
<b>McastReleaseAddress</b> function returns the status of the operation.

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



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrenewaddress">McastRenewAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>