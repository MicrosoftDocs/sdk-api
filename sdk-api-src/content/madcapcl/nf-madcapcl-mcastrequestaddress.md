---
UID: NF:madcapcl.McastRequestAddress
title: McastRequestAddress function
author: windows-sdk-content
description: The McastRequestAddress function requests one or more multicast addresses from a MADCAP server.
old-location: madcap\mcastrequestaddress.htm
tech.root: madcap
ms.assetid: 856eb251-1909-41a1-8e4f-c081942280de
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: McastRequestAddress, McastRequestAddress function [MADCAP], _mdhcp_mcastrequestaddress, madcap.mcastrequestaddress, madcapcl/McastRequestAddress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpcsvc.dll
api_name:
 - McastRequestAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# McastRequestAddress function


## -description


The 
<b>McastRequestAddress</b> function requests one or more multicast addresses from a MADCAP server.


## -parameters




### -param AddrFamily [in]

Specifies the address family to be used in the request, in the form of an 
<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a> structure. Use AF_INET for IPv4 addresses and AF_INET6 for IPv6 addresses.


### -param pRequestID [in]

Pointer to a unique identifier for the request, in the form of an 
<a href="https://msdn.microsoft.com/6460ea80-f1b1-4939-a977-580d0db10fd0">MCAST_CLIENT_UID</a> structure. Clients are responsible for ensuring that each request contains a unique identifier; unique identifiers can be obtained by calling the 
<a href="https://msdn.microsoft.com/67d5f149-d9b3-4903-a859-1ad33e310997">McastGenUID</a> function.


### -param pScopeCtx [in]

Pointer to the context of the scope from which the address is to be allocated, in the form of an 
<a href="https://msdn.microsoft.com/164d8f73-f5f5-4cc6-85ca-8e249192c202">MCAST_SCOPE_CTX</a> structure. The scope context must be retrieved by calling the 
<a href="https://msdn.microsoft.com/df33d766-d420-4069-8b94-86f5e4e91c1d">McastEnumerateScopes</a> function prior to calling the 
<b>McastRequestAddress</b> function.


### -param pAddrRequest [in]

Pointer to the 
<a href="https://msdn.microsoft.com/3110a1f3-e252-4eab-bf69-cbecfd65a5e0">MCAST_LEASE_REQUEST</a> structure containing multicast lease–request parameters.


### -param pAddrResponse [in, out]

Pointer to a buffer containing response parameters for the multicast address request, in the form of an 
<a href="https://msdn.microsoft.com/1993e3bc-b6bd-4e13-aa71-7e33bf7ef540">MCAST_LEASE_RESPONSE</a> structure. The caller is responsible for allocating sufficient buffer space for the <i>pAddrBuf</i> member of the 
<b>MCAST_LEASE_RESPONSE</b> structure to hold the requested number of addresses; the caller is also responsible for setting the pointer to that buffer.


## -returns



The 
<b>McastRequestAddress</b> function returns the status of the operation.




## -remarks



Before the 
<b>McastRequestAddress</b> function is called, the scope context must be retrieved by calling the 
<a href="https://msdn.microsoft.com/df33d766-d420-4069-8b94-86f5e4e91c1d">McastEnumerateScopes</a> function.




## -see-also




<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a>



<a href="https://msdn.microsoft.com/6460ea80-f1b1-4939-a977-580d0db10fd0">MCAST_CLIENT_UID</a>



<a href="https://msdn.microsoft.com/3110a1f3-e252-4eab-bf69-cbecfd65a5e0">MCAST_LEASE_REQUEST</a>



<a href="https://msdn.microsoft.com/1993e3bc-b6bd-4e13-aa71-7e33bf7ef540">MCAST_LEASE_RESPONSE</a>



<a href="https://msdn.microsoft.com/164d8f73-f5f5-4cc6-85ca-8e249192c202">MCAST_SCOPE_CTX</a>



<a href="https://msdn.microsoft.com/d275e78b-ddf3-4f92-a76f-463aec2f6c95">MCAST_SCOPE_ENTRY</a>



<a href="https://msdn.microsoft.com/eccf52ee-8145-4a8f-9d34-5a56bfc8a48c">McastApiCleanup</a>



<a href="https://msdn.microsoft.com/edb7d666-cbd0-46f7-b63e-2a09ffc9e9e2">McastApiStartup</a>



<a href="https://msdn.microsoft.com/df33d766-d420-4069-8b94-86f5e4e91c1d">McastEnumerateScopes</a>



<a href="https://msdn.microsoft.com/67d5f149-d9b3-4903-a859-1ad33e310997">McastGenUID</a>



<a href="https://msdn.microsoft.com/6cb87e3b-0d2e-46f8-8ccf-6309c8fb888c">McastReleaseAddress</a>



<a href="https://msdn.microsoft.com/d1d26edb-f372-4d6d-a6e2-a8eeafadedc0">McastRenewAddress</a>
 

 

