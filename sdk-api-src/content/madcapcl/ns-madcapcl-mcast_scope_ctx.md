---
UID: NS:madcapcl._MCAST_SCOPE_CTX
title: MCAST_SCOPE_CTX (madcapcl.h)
description: The MCAST_SCOPE_CTX structure defines the scope context for programmatic interaction with multicast addresses. The MCAST_SCOPE_CTX structure is used by various MADCAP functions as a handle for allocating, renewing, or releasing MADCAP addresses.
helpviewer_keywords: ["*PMCAST_SCOPE_CTX","MCAST_SCOPE_CTX","MCAST_SCOPE_CTX structure [MADCAP]","PMCAST_SCOPE_CTX","PMCAST_SCOPE_CTX structure pointer [MADCAP]","_mdhcp_mcast_scope_ctx","madcap.mcast_scope_ctx","madcapcl/MCAST_SCOPE_CTX","madcapcl/PMCAST_SCOPE_CTX"]
old-location: madcap\mcast_scope_ctx.htm
tech.root: Madcap
ms.assetid: 164d8f73-f5f5-4cc6-85ca-8e249192c202
ms.date: 12/05/2018
ms.keywords: '*PMCAST_SCOPE_CTX, MCAST_SCOPE_CTX, MCAST_SCOPE_CTX structure [MADCAP], PMCAST_SCOPE_CTX, PMCAST_SCOPE_CTX structure pointer [MADCAP], _mdhcp_mcast_scope_ctx, madcap.mcast_scope_ctx, madcapcl/MCAST_SCOPE_CTX, madcapcl/PMCAST_SCOPE_CTX'
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
req.typenames: MCAST_SCOPE_CTX, *PMCAST_SCOPE_CTX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MCAST_SCOPE_CTX
 - madcapcl/_MCAST_SCOPE_CTX
 - PMCAST_SCOPE_CTX
 - madcapcl/PMCAST_SCOPE_CTX
 - MCAST_SCOPE_CTX
 - madcapcl/MCAST_SCOPE_CTX
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
 - MCAST_SCOPE_CTX
---

# MCAST_SCOPE_CTX structure


## -description

The 
<b>MCAST_SCOPE_CTX</b> structure defines the scope context for programmatic interaction with multicast addresses. The 
<b>MCAST_SCOPE_CTX</b> structure is used by various MADCAP functions as a handle for allocating, renewing, or releasing MADCAP addresses.

## -struct-fields

### -field ScopeID

Identifier for the multicast scope, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a> structure.

### -field Interface

Interface on which the multicast scope is available, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a> structure.

### -field ServerID

Internet Protocol (IP) address of the MADCAP server, in the form of an 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a> structure.

## -see-also

<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_client_uid">MCAST_CLIENT_UID</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_request">MCAST_LEASE_REQUEST</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_response">MCAST_LEASE_RESPONSE</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_entry">MCAST_SCOPE_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapicleanup">McastApiCleanup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapistartup">McastApiStartup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastenumeratescopes">McastEnumerateScopes</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastgenuid">McastGenUID</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastreleaseaddress">McastReleaseAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrenewaddress">McastRenewAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>