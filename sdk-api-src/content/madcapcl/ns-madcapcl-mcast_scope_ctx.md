---
UID: NS:madcapcl._MCAST_SCOPE_CTX
title: MCAST_SCOPE_CTX
author: windows-sdk-content
description: The MCAST_SCOPE_CTX structure defines the scope context for programmatic interaction with multicast addresses. The MCAST_SCOPE_CTX structure is used by various MADCAP functions as a handle for allocating, renewing, or releasing MADCAP addresses.
old-location: madcap\mcast_scope_ctx.htm
tech.root: Madcap
ms.assetid: 164d8f73-f5f5-4cc6-85ca-8e249192c202
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMCAST_SCOPE_CTX, MCAST_SCOPE_CTX, MCAST_SCOPE_CTX structure [MADCAP], PMCAST_SCOPE_CTX, PMCAST_SCOPE_CTX structure pointer [MADCAP], _mdhcp_mcast_scope_ctx, madcap.mcast_scope_ctx, madcapcl/MCAST_SCOPE_CTX, madcapcl/PMCAST_SCOPE_CTX"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Madcapcl.h
api_name:
 - MCAST_SCOPE_CTX
product: Windows
targetos: Windows
req.typenames: MCAST_SCOPE_CTX, *PMCAST_SCOPE_CTX
req.redist: 
---

# MCAST_SCOPE_CTX structure


## -description


The 
<b>MCAST_SCOPE_CTX</b> structure defines the scope context for programmatic interaction with multicast addresses. The 
<b>MCAST_SCOPE_CTX</b> structure is used by various MADCAP functions as a handle for allocating, renewing, or releasing MADCAP addresses.


## -struct-fields




### -field ScopeID

Identifier for the multicast scope, in the form of an 
<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a> structure.


### -field Interface

Interface on which the multicast scope is available, in the form of an 
<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a> structure.


### -field ServerID

Internet Protocol (IP) address of the MADCAP server, in the form of an 
<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a>



<a href="https://msdn.microsoft.com/6460ea80-f1b1-4939-a977-580d0db10fd0">MCAST_CLIENT_UID</a>



<a href="https://msdn.microsoft.com/3110a1f3-e252-4eab-bf69-cbecfd65a5e0">MCAST_LEASE_REQUEST</a>



<a href="https://msdn.microsoft.com/1993e3bc-b6bd-4e13-aa71-7e33bf7ef540">MCAST_LEASE_RESPONSE</a>



<a href="https://msdn.microsoft.com/d275e78b-ddf3-4f92-a76f-463aec2f6c95">MCAST_SCOPE_ENTRY</a>



<a href="https://msdn.microsoft.com/eccf52ee-8145-4a8f-9d34-5a56bfc8a48c">McastApiCleanup</a>



<a href="https://msdn.microsoft.com/edb7d666-cbd0-46f7-b63e-2a09ffc9e9e2">McastApiStartup</a>



<a href="https://msdn.microsoft.com/df33d766-d420-4069-8b94-86f5e4e91c1d">McastEnumerateScopes</a>



<a href="https://msdn.microsoft.com/67d5f149-d9b3-4903-a859-1ad33e310997">McastGenUID</a>



<a href="https://msdn.microsoft.com/6cb87e3b-0d2e-46f8-8ccf-6309c8fb888c">McastReleaseAddress</a>



<a href="https://msdn.microsoft.com/d1d26edb-f372-4d6d-a6e2-a8eeafadedc0">McastRenewAddress</a>



<a href="https://msdn.microsoft.com/856eb251-1909-41a1-8e4f-c081942280de">McastRequestAddress</a>
 

 

