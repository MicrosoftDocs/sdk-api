---
UID: NS:madcapcl._MCAST_LEASE_RESPONSE
title: MCAST_LEASE_RESPONSE (madcapcl.h)
description: The MCAST_LEASE_RESPONSE structure is used to respond to multicast lease requests.
helpviewer_keywords: ["*PMCAST_LEASE_RESPONSE","MCAST_LEASE_RESPONSE","MCAST_LEASE_RESPONSE structure [MADCAP]","PMCAST_LEASE_RESPONSE","PMCAST_LEASE_RESPONSE structure pointer [MADCAP]","_mdhcp_mcast_lease_response","madcap.mcast_lease_response","madcapcl/MCAST_LEASE_RESPONSE","madcapcl/PMCAST_LEASE_RESPONSE"]
old-location: madcap\mcast_lease_response.htm
tech.root: Madcap
ms.assetid: 1993e3bc-b6bd-4e13-aa71-7e33bf7ef540
ms.date: 12/05/2018
ms.keywords: '*PMCAST_LEASE_RESPONSE, MCAST_LEASE_RESPONSE, MCAST_LEASE_RESPONSE structure [MADCAP], PMCAST_LEASE_RESPONSE, PMCAST_LEASE_RESPONSE structure pointer [MADCAP], _mdhcp_mcast_lease_response, madcap.mcast_lease_response, madcapcl/MCAST_LEASE_RESPONSE, madcapcl/PMCAST_LEASE_RESPONSE'
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
req.typenames: MCAST_LEASE_RESPONSE, *PMCAST_LEASE_RESPONSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MCAST_LEASE_RESPONSE
 - madcapcl/_MCAST_LEASE_RESPONSE
 - PMCAST_LEASE_RESPONSE
 - madcapcl/PMCAST_LEASE_RESPONSE
 - MCAST_LEASE_RESPONSE
 - madcapcl/MCAST_LEASE_RESPONSE
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
 - MCAST_LEASE_RESPONSE
---

# MCAST_LEASE_RESPONSE structure


## -description

The 
<b>MCAST_LEASE_RESPONSE</b> structure is used to respond to multicast lease requests.

## -struct-fields

### -field LeaseStartTime

Start time, in seconds, for the multicast scope lease elapsed since midnight of January 1, 1970, coordinated universal time.

### -field LeaseEndTime

Expiration time, in seconds of the multicast scope lease elapsed since midnight of January 1, 1970, coordinated universal time.

### -field ServerAddress

Internet Protocol (IP) address of the server on which the lease request has been granted or renewed, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a> structure.

### -field AddrCount

Number of IP addresses that are granted or renewed with the lease. Note that the value of this member dictates the size of <b>pAddrBuf</b>.

### -field pAddrBuf

Pointer to a buffer containing the granted IP addresses. For IPv4 addresses, the <b>pAddrBuf</b> member points to 4-byte addresses; for IPv6 addresses, the <b>pAddrBuf</b> member points to 16-byte addresses.

## -see-also

<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_client_uid">MCAST_CLIENT_UID</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_request">MCAST_LEASE_REQUEST</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_ctx">MCAST_SCOPE_CTX</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_entry">MCAST_SCOPE_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapicleanup">McastApiCleanup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapistartup">McastApiStartup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastenumeratescopes">McastEnumerateScopes</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastgenuid">McastGenUID</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>