---
UID: NS:madcapcl._MCAST_LEASE_RESPONSE
title: "_MCAST_LEASE_RESPONSE"
author: windows-sdk-content
description: The MCAST_LEASE_RESPONSE structure is used to respond to multicast lease requests.
old-location: madcap\mcast_lease_response.htm
tech.root: Madcap
ms.assetid: 1993e3bc-b6bd-4e13-aa71-7e33bf7ef540
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PMCAST_LEASE_RESPONSE, MCAST_LEASE_RESPONSE, MCAST_LEASE_RESPONSE structure [MADCAP], PMCAST_LEASE_RESPONSE, PMCAST_LEASE_RESPONSE structure pointer [MADCAP], _MCAST_LEASE_RESPONSE, _mdhcp_mcast_lease_response, madcap.mcast_lease_response, madcapcl/MCAST_LEASE_RESPONSE, madcapcl/PMCAST_LEASE_RESPONSE"
ms.prod: windows
ms.technology: windows-sdk
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
 - MCAST_LEASE_RESPONSE
product: Windows
targetos: Windows
req.typenames: MCAST_LEASE_RESPONSE, *PMCAST_LEASE_RESPONSE
req.redist: 
---

# _MCAST_LEASE_RESPONSE structure


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
<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a> structure.


### -field AddrCount

Number of IP addresses that are granted or renewed with the lease. Note that the value of this member dictates the size of <b>pAddrBuf</b>.


### -field pAddrBuf

Pointer to a buffer containing the granted IP addresses. For IPv4 addresses, the <b>pAddrBuf</b> member points to 4-byte addresses; for IPv6 addresses, the <b>pAddrBuf</b> member points to 16-byte addresses.


## -see-also




<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a>



<a href="https://msdn.microsoft.com/6460ea80-f1b1-4939-a977-580d0db10fd0">MCAST_CLIENT_UID</a>



<a href="https://msdn.microsoft.com/3110a1f3-e252-4eab-bf69-cbecfd65a5e0">MCAST_LEASE_REQUEST</a>



<a href="https://msdn.microsoft.com/164d8f73-f5f5-4cc6-85ca-8e249192c202">MCAST_SCOPE_CTX</a>



<a href="https://msdn.microsoft.com/d275e78b-ddf3-4f92-a76f-463aec2f6c95">MCAST_SCOPE_ENTRY</a>



<a href="https://msdn.microsoft.com/eccf52ee-8145-4a8f-9d34-5a56bfc8a48c">McastApiCleanup</a>



<a href="https://msdn.microsoft.com/edb7d666-cbd0-46f7-b63e-2a09ffc9e9e2">McastApiStartup</a>



<a href="https://msdn.microsoft.com/df33d766-d420-4069-8b94-86f5e4e91c1d">McastEnumerateScopes</a>



<a href="https://msdn.microsoft.com/67d5f149-d9b3-4903-a859-1ad33e310997">McastGenUID</a>



<a href="https://msdn.microsoft.com/856eb251-1909-41a1-8e4f-c081942280de">McastRequestAddress</a>
 

 

