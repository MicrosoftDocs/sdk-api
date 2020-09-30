---
UID: NF:madcapcl.McastGenUID
title: McastGenUID function (madcapcl.h)
description: The McastGenUID function generates a unique identifier, subsequently used by clients to request and renew addresses.
helpviewer_keywords: ["McastGenUID","McastGenUID function [MADCAP]","_mdhcp_mcastgenuid","madcap.mcastgenuid","madcapcl/McastGenUID"]
old-location: madcap\mcastgenuid.htm
tech.root: Madcap
ms.assetid: 67d5f149-d9b3-4903-a859-1ad33e310997
ms.date: 12/05/2018
ms.keywords: McastGenUID, McastGenUID function [MADCAP], _mdhcp_mcastgenuid, madcap.mcastgenuid, madcapcl/McastGenUID
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
 - McastGenUID
 - madcapcl/McastGenUID
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
 - McastGenUID
---

# McastGenUID function


## -description

The 
<b>McastGenUID</b> function generates a unique identifier, subsequently used by clients to request and renew addresses.

## -parameters

### -param pRequestID [in]

Pointer to the 
<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_client_uid">MCAST_CLIENT_UID</a> structure into which the unique identifier is stored. The size of the buffer to which <i>pRequestID</i> points must be at least MCAST_CLIENT_ID_LEN in size.

## -returns

The 
<b>McastGenUID</b> function returns the status of the operation.

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



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastreleaseaddress">McastReleaseAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrenewaddress">McastRenewAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>