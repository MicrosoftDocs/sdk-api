---
UID: NS:madcapcl._MCAST_SCOPE_ENTRY
title: MCAST_SCOPE_ENTRY (madcapcl.h)
description: The MCAST_SCOPE_ENTRY structure provides a complete set of information about a given multicast scope.
helpviewer_keywords: ["*PMCAST_SCOPE_ENTRY","MCAST_SCOPE_ENTRY","MCAST_SCOPE_ENTRY structure [MADCAP]","PMCAST_SCOPE_ENTRY","PMCAST_SCOPE_ENTRY structure pointer [MADCAP]","_mdhcp_mcast_scope_entry","madcap.mcast_scope_entry","madcapcl/MCAST_SCOPE_ENTRY","madcapcl/PMCAST_SCOPE_ENTRY"]
old-location: madcap\mcast_scope_entry.htm
tech.root: Madcap
ms.assetid: d275e78b-ddf3-4f92-a76f-463aec2f6c95
ms.date: 12/05/2018
ms.keywords: '*PMCAST_SCOPE_ENTRY, MCAST_SCOPE_ENTRY, MCAST_SCOPE_ENTRY structure [MADCAP], PMCAST_SCOPE_ENTRY, PMCAST_SCOPE_ENTRY structure pointer [MADCAP], _mdhcp_mcast_scope_entry, madcap.mcast_scope_entry, madcapcl/MCAST_SCOPE_ENTRY, madcapcl/PMCAST_SCOPE_ENTRY'
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
req.typenames: MCAST_SCOPE_ENTRY, *PMCAST_SCOPE_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MCAST_SCOPE_ENTRY
 - madcapcl/_MCAST_SCOPE_ENTRY
 - PMCAST_SCOPE_ENTRY
 - madcapcl/PMCAST_SCOPE_ENTRY
 - MCAST_SCOPE_ENTRY
 - madcapcl/MCAST_SCOPE_ENTRY
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
 - MCAST_SCOPE_ENTRY
---

# MCAST_SCOPE_ENTRY structure


## -description

The 
<b>MCAST_SCOPE_ENTRY</b> structure provides a complete set of information about a given multicast scope.

## -struct-fields

### -field ScopeCtx

Handle for the multicast scope, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_ctx">MCAST_SCOPE_CTX</a> structure.

### -field LastAddr

Internet Protocol (IP) address of the last address in the scope, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a> structure.

### -field TTL

Time To Live (TTL) value of the scope.

### -field ScopeDesc

Description of the scope, in human readable, user-friendly format.

## -see-also

<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_client_uid">MCAST_CLIENT_UID</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_request">MCAST_LEASE_REQUEST</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_response">MCAST_LEASE_RESPONSE</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_ctx">MCAST_SCOPE_CTX</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapicleanup">McastApiCleanup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapistartup">McastApiStartup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastenumeratescopes">McastEnumerateScopes</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastgenuid">McastGenUID</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastreleaseaddress">McastReleaseAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrenewaddress">McastRenewAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>



<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a>