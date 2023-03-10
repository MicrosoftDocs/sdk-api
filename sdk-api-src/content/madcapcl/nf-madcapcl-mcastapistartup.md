---
UID: NF:madcapcl.McastApiStartup
title: McastApiStartup function (madcapcl.h)
description: The McastApiStartup function facilitates MADCAP-version negotiation between requesting clients and the version of MADCAP implemented on the system.
helpviewer_keywords: ["McastApiStartup","McastApiStartup function [MADCAP]","_mdhcp_mcastapistartup","madcap.mcastapistartup","madcapcl/McastApiStartup"]
old-location: madcap\mcastapistartup.htm
tech.root: Madcap
ms.assetid: edb7d666-cbd0-46f7-b63e-2a09ffc9e9e2
ms.date: 12/05/2018
ms.keywords: McastApiStartup, McastApiStartup function [MADCAP], _mdhcp_mcastapistartup, madcap.mcastapistartup, madcapcl/McastApiStartup
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
 - McastApiStartup
 - madcapcl/McastApiStartup
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
 - McastApiStartup
---

# McastApiStartup function


## -description

The 
<b>McastApiStartup</b> function facilitates MADCAP-version negotiation between requesting clients and the version of MADCAP implemented on the system. Calling 
<b>McastApiStartup</b> allocates necessary resources; it must be called before any other MADCAP client functions are called.

## -parameters

### -param Version [in]

Pointer to the version of multicast (MCAST) that the client wishes to use. 




[out] Pointer to the version of MCAST implemented on the system.

## -returns

If the client requests a version of MADCAP that is not supported by the system, the 
<b>McastApiStartup</b> function returns ERROR_NOT_SUPPORTED. If resources fail to be allocated for the function call, ERROR_NO_SYSTEM_RESOURCES is returned.

## -remarks

Clients can specify which version they want to use in the <i>pVersion</i> parameter. If the system's implementation supports the requested MCAST version, the function call succeeds. If the system's implementation does not support the requested version, the function fails with MCAST_API_CURRENT_VERSION.

The client can automatically negotiate the first version of MCAST (MCAST_API_VERSION_1) by setting the <i>pVersion</i> parameter to zero.

The 
<b>McastApiStartup</b> function always returns the most recent version of MADCAP available on the system (MCAST_API_CURRENT_VERSION) in <i>pVersion</i>, enabling clients to discover the most recent version implemented on the system.

## -see-also

<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_client_uid">MCAST_CLIENT_UID</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_request">MCAST_LEASE_REQUEST</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_response">MCAST_LEASE_RESPONSE</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_ctx">MCAST_SCOPE_CTX</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_entry">MCAST_SCOPE_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapicleanup">McastApiCleanup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastenumeratescopes">McastEnumerateScopes</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastgenuid">McastGenUID</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastreleaseaddress">McastReleaseAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrenewaddress">McastRenewAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>