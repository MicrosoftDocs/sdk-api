---
UID: NS:madcapcl._IPNG_ADDRESS
title: IPNG_ADDRESS (madcapcl.h)
description: The IPNG_ADDRESS union provides Internet Protocol version 4 (IPv4) and Internet Protocol version 6 (IPv6) addresses.
helpviewer_keywords: ["*PIPNG_ADDRESS","IPNG_ADDRESS","IPNG_ADDRESS union [MADCAP]","PIPNG_ADDRESS","PIPNG_ADDRESS union pointer [MADCAP]","_mdhcp_ipng_address","madcap.ipng_address","madcapcl/IPNG_ADDRESS","madcapcl/PIPNG_ADDRESS"]
old-location: madcap\ipng_address.htm
tech.root: Madcap
ms.assetid: c3dc76aa-d903-49be-a4a2-1f66cafff40a
ms.date: 12/05/2018
ms.keywords: '*PIPNG_ADDRESS, IPNG_ADDRESS, IPNG_ADDRESS union [MADCAP], PIPNG_ADDRESS, PIPNG_ADDRESS union pointer [MADCAP], _mdhcp_ipng_address, madcap.ipng_address, madcapcl/IPNG_ADDRESS, madcapcl/PIPNG_ADDRESS'
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
req.typenames: IPNG_ADDRESS, *PIPNG_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IPNG_ADDRESS
 - madcapcl/_IPNG_ADDRESS
 - PIPNG_ADDRESS
 - madcapcl/PIPNG_ADDRESS
 - IPNG_ADDRESS
 - madcapcl/IPNG_ADDRESS
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
 - IPNG_ADDRESS
---

# IPNG_ADDRESS structure


## -description

The 
<b>IPNG_ADDRESS</b> union provides Internet Protocol version 4 (IPv4) and Internet Protocol version 6 (IPv6) addresses.

## -struct-fields

### -field IpAddrV4

Internet Protocol (IP) address, in version 4 format (IPv4).

### -field IpAddrV6

Internet Protocol (IP) address, in version 6 format (IPv6).

## -see-also

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



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>