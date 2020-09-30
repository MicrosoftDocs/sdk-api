---
UID: NS:madcapcl._MCAST_LEASE_REQUEST
title: MCAST_LEASE_REQUEST (madcapcl.h)
description: The MCAST_LEASE_REQUEST structure defines the request, renew, or release parameters for a given multicast scope. In the MCAST_API_VERSION_1 implementation, only one IP address may be allocated at a time.
helpviewer_keywords: ["*PMCAST_LEASE_REQUEST","MCAST_LEASE_REQUEST","MCAST_LEASE_REQUEST structure [MADCAP]","PMCAST_LEASE_REQUEST","PMCAST_LEASE_REQUEST structure pointer [MADCAP]","_mdhcp_mcast_lease_request","madcap.mcast_lease_request","madcapcl/MCAST_LEASE_REQUEST","madcapcl/PMCAST_LEASE_REQUEST"]
old-location: madcap\mcast_lease_request.htm
tech.root: Madcap
ms.assetid: 3110a1f3-e252-4eab-bf69-cbecfd65a5e0
ms.date: 12/05/2018
ms.keywords: '*PMCAST_LEASE_REQUEST, MCAST_LEASE_REQUEST, MCAST_LEASE_REQUEST structure [MADCAP], PMCAST_LEASE_REQUEST, PMCAST_LEASE_REQUEST structure pointer [MADCAP], _mdhcp_mcast_lease_request, madcap.mcast_lease_request, madcapcl/MCAST_LEASE_REQUEST, madcapcl/PMCAST_LEASE_REQUEST'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MCAST_LEASE_REQUEST, *PMCAST_LEASE_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MCAST_LEASE_REQUEST
 - madcapcl/_MCAST_LEASE_REQUEST
 - PMCAST_LEASE_REQUEST
 - madcapcl/PMCAST_LEASE_REQUEST
 - MCAST_LEASE_REQUEST
 - madcapcl/MCAST_LEASE_REQUEST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Madcapcl.h
api_name:
 - MCAST_LEASE_REQUEST
---

# MCAST_LEASE_REQUEST structure


## -description

The 
<b>MCAST_LEASE_REQUEST</b> structure defines the request, renew, or release parameters for a given multicast scope. In the MCAST_API_VERSION_1 implementation, only one IP address may be allocated at a time.

## -struct-fields

### -field LeaseStartTime

Requested start time, in seconds, for the multicast scope lease elapsed since midnight of January 1, 1970, coordinated universal time. To request the current time as the lease start time, set <b>LeaseStartTime</b> to zero.

### -field MaxLeaseStartTime

Maximum start time, in seconds, elapsed since midnight of January 1, 1970, coordinated universal time, that the client is willing to accept.

### -field LeaseDuration

Duration of the lease request, in seconds. To request the default lease duration, set both <b>LeaseDuration</b> and <b>MinLeaseDuration</b> to zero.

### -field MinLeaseDuration

Minimum lease duration, in seconds, that the client is willing to accept.

### -field ServerAddress

Internet Protocol (IP) address of the server on which the lease is to be requested or renewed, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a> structure. If the IP address of the server is unknown, such as when using this structure in an 
<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a> function call, set <b>ServerAddress</b> to zero.

### -field MinAddrCount

Minimum number of IP addresses the client is willing to accept.

### -field AddrCount

Number of requested IP addresses. Note that the value of this member dictates the size of <b>pAddrBuf</b>.

### -field pAddrBuf

Pointer to a buffer containing the requested IP addresses. For IPv4 addresses, the <b>pAddrBuf</b> member points to 4-byte addresses; for IPv6 addresses, the <b>pAddrBuf</b> member points to 16-byte addresses. If no specific addresses are requested, set <b>pAddrBuf</b> to <b>NULL</b>.

## -remarks

In MCAST_API_VERSION_1 version, <b>MaxLeaseStartTime</b>, <b>MinLeaseDuration</b>, and <b>MinAddrCount</b> members are ignored. Clients should still set appropriate values for these members, however, to take advantage of their implementation in future updates.

## -see-also

<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_client_uid">MCAST_CLIENT_UID</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_response">MCAST_LEASE_RESPONSE</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_ctx">MCAST_SCOPE_CTX</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_entry">MCAST_SCOPE_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapicleanup">McastApiCleanup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapistartup">McastApiStartup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastenumeratescopes">McastEnumerateScopes</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastgenuid">McastGenUID</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>