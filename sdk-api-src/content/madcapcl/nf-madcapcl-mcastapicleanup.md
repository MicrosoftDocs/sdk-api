---
UID: NF:madcapcl.McastApiCleanup
title: McastApiCleanup function (madcapcl.h)
description: The McastApiCleanup function deallocates resources that are allocated with McastApiStartup. The McastApiCleanup function must only be called after a successful call to McastApiStartup.
helpviewer_keywords: ["McastApiCleanup","McastApiCleanup function [MADCAP]","_mdhcp_mcastapicleanup","madcap.mcastapicleanup","madcapcl/McastApiCleanup"]
old-location: madcap\mcastapicleanup.htm
tech.root: Madcap
ms.assetid: eccf52ee-8145-4a8f-9d34-5a56bfc8a48c
ms.date: 12/05/2018
ms.keywords: McastApiCleanup, McastApiCleanup function [MADCAP], _mdhcp_mcastapicleanup, madcap.mcastapicleanup, madcapcl/McastApiCleanup
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
 - McastApiCleanup
 - madcapcl/McastApiCleanup
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
 - McastApiCleanup
---

# McastApiCleanup function


## -description

The 
<b>McastApiCleanup</b> function deallocates resources that are allocated with 
<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapistartup">McastApiStartup</a>. The 
<b>McastApiCleanup</b> function must only be called after a successful call to 
<b>McastApiStartup</b>.



## -see-also

<a href="/windows/desktop/api/madcapcl/ns-madcapcl-ipng_address">IPNG_ADDRESS</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_client_uid">MCAST_CLIENT_UID</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_request">MCAST_LEASE_REQUEST</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_lease_response">MCAST_LEASE_RESPONSE</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_ctx">MCAST_SCOPE_CTX</a>



<a href="/windows/desktop/api/madcapcl/ns-madcapcl-mcast_scope_entry">MCAST_SCOPE_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastapistartup">McastApiStartup</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastenumeratescopes">McastEnumerateScopes</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastgenuid">McastGenUID</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastreleaseaddress">McastReleaseAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrenewaddress">McastRenewAddress</a>



<a href="/previous-versions/windows/desktop/api/madcapcl/nf-madcapcl-mcastrequestaddress">McastRequestAddress</a>
