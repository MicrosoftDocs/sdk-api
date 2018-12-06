---
UID: NS:madcapcl._MCAST_SCOPE_ENTRY
title: "_MCAST_SCOPE_ENTRY"
author: windows-sdk-content
description: The MCAST_SCOPE_ENTRY structure provides a complete set of information about a given multicast scope.
old-location: madcap\mcast_scope_entry.htm
tech.root: Madcap
ms.assetid: d275e78b-ddf3-4f92-a76f-463aec2f6c95
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMCAST_SCOPE_ENTRY, MCAST_SCOPE_ENTRY, MCAST_SCOPE_ENTRY structure [MADCAP], PMCAST_SCOPE_ENTRY, PMCAST_SCOPE_ENTRY structure pointer [MADCAP], _MCAST_SCOPE_ENTRY, _mdhcp_mcast_scope_entry, madcap.mcast_scope_entry, madcapcl/MCAST_SCOPE_ENTRY, madcapcl/PMCAST_SCOPE_ENTRY"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MCAST_SCOPE_ENTRY
product: Windows
targetos: Windows
req.typenames: MCAST_SCOPE_ENTRY, *PMCAST_SCOPE_ENTRY
req.redist: 
---

# _MCAST_SCOPE_ENTRY structure


## -description


The 
<b>MCAST_SCOPE_ENTRY</b> structure provides a complete set of information about a given multicast scope.


## -struct-fields




### -field ScopeCtx

Handle for the multicast scope, in the form of an 
<a href="https://msdn.microsoft.com/164d8f73-f5f5-4cc6-85ca-8e249192c202">MCAST_SCOPE_CTX</a> structure.


### -field LastAddr

Internet Protocol (IP) address of the last address in the scope, in the form of an 
<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a> structure.


### -field TTL

Time To Live (TTL) value of the scope.


### -field ScopeDesc

Description of the scope, in human readable, user-friendly format.


## -see-also




<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a>



<a href="https://msdn.microsoft.com/6460ea80-f1b1-4939-a977-580d0db10fd0">MCAST_CLIENT_UID</a>



<a href="https://msdn.microsoft.com/3110a1f3-e252-4eab-bf69-cbecfd65a5e0">MCAST_LEASE_REQUEST</a>



<a href="https://msdn.microsoft.com/1993e3bc-b6bd-4e13-aa71-7e33bf7ef540">MCAST_LEASE_RESPONSE</a>



<a href="https://msdn.microsoft.com/164d8f73-f5f5-4cc6-85ca-8e249192c202">MCAST_SCOPE_CTX</a>



<a href="https://msdn.microsoft.com/eccf52ee-8145-4a8f-9d34-5a56bfc8a48c">McastApiCleanup</a>



<a href="https://msdn.microsoft.com/edb7d666-cbd0-46f7-b63e-2a09ffc9e9e2">McastApiStartup</a>



<a href="https://msdn.microsoft.com/df33d766-d420-4069-8b94-86f5e4e91c1d">McastEnumerateScopes</a>



<a href="https://msdn.microsoft.com/67d5f149-d9b3-4903-a859-1ad33e310997">McastGenUID</a>



<a href="https://msdn.microsoft.com/6cb87e3b-0d2e-46f8-8ccf-6309c8fb888c">McastReleaseAddress</a>



<a href="https://msdn.microsoft.com/d1d26edb-f372-4d6d-a6e2-a8eeafadedc0">McastRenewAddress</a>



<a href="https://msdn.microsoft.com/856eb251-1909-41a1-8e4f-c081942280de">McastRequestAddress</a>



<a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a>
 

 

