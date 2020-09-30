---
UID: NS:madcapcl._MCAST_CLIENT_UID
title: MCAST_CLIENT_UID (madcapcl.h)
description: The MCAST_CLIENT_UID structure describes the unique client identifier for each multicast request.
helpviewer_keywords: ["*LPMCAST_CLIENT_UID","LPMCAST_CLIENT_UID","LPMCAST_CLIENT_UID structure pointer [MADCAP]","MCAST_CLIENT_UID","MCAST_CLIENT_UID structure [MADCAP]","_mdhcp_mcast_client_uid","madcap.mcast_client_uid","madcapcl/LPMCAST_CLIENT_UID","madcapcl/MCAST_CLIENT_UID"]
old-location: madcap\mcast_client_uid.htm
tech.root: Madcap
ms.assetid: 6460ea80-f1b1-4939-a977-580d0db10fd0
ms.date: 12/05/2018
ms.keywords: '*LPMCAST_CLIENT_UID, LPMCAST_CLIENT_UID, LPMCAST_CLIENT_UID structure pointer [MADCAP], MCAST_CLIENT_UID, MCAST_CLIENT_UID structure [MADCAP], _mdhcp_mcast_client_uid, madcap.mcast_client_uid, madcapcl/LPMCAST_CLIENT_UID, madcapcl/MCAST_CLIENT_UID'
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
req.typenames: MCAST_CLIENT_UID, *LPMCAST_CLIENT_UID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MCAST_CLIENT_UID
 - madcapcl/_MCAST_CLIENT_UID
 - LPMCAST_CLIENT_UID
 - madcapcl/LPMCAST_CLIENT_UID
 - MCAST_CLIENT_UID
 - madcapcl/MCAST_CLIENT_UID
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
 - MCAST_CLIENT_UID
---

# MCAST_CLIENT_UID structure


## -description

The 
<b>MCAST_CLIENT_UID</b> structure describes the unique client identifier for each multicast request.

## -struct-fields

### -field ClientUID

Buffer containing the unique client identifier.

### -field ClientUIDLength

Size of the <b>ClientUID</b> member, in bytes.

## -see-also

<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_request">MCAST_LEASE_REQUEST</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_ctx">MCAST_SCOPE_CTX</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_entry">MCAST_SCOPE_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapicleanup">McastApiCleanup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapistartup">McastApiStartup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastenumeratescopes">McastEnumerateScopes</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastgenuid">McastGenUID</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>