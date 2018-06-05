---
UID: NF:madcapcl.McastEnumerateScopes
title: McastEnumerateScopes function
author: windows-sdk-content
description: The McastEnumerateScopes function enumerates multicast scopes available on the network.
old-location: madcap\mcastenumeratescopes.htm
old-project: Madcap
ms.assetid: df33d766-d420-4069-8b94-86f5e4e91c1d
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: McastEnumerateScopes, McastEnumerateScopes function [MADCAP], _mdhcp_mcastenumeratescopes, madcap.mcastenumeratescopes, madcapcl/McastEnumerateScopes
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: POLICY_DNS_DOMAIN_INFO, *PPOLICY_DNS_DOMAIN_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpcsvc.dll
api_name:
-	McastEnumerateScopes
product: Windows
targetos: Windows
req.lib: Dhcpcsvc.lib
req.dll: Dhcpcsvc.dll
req.irql: 
req.product: GDI+ 1.1
---

# McastEnumerateScopes function


## -description


The 
<b>McastEnumerateScopes</b> function enumerates multicast scopes available on the network.


## -parameters




### -param AddrFamily [in]

Specifies the address family to be used in enumeration, in the form of an 
<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a> structure. Use AF_INET for IPv4 addresses and AF_INET6 for IPv6 addresses.


### -param ReQuery [in]

Enables a caller to query a list again. Set this parameter to <b>TRUE</b> if the list is to be queried more than once. Otherwise, set it to <b>FALSE</b>.


### -param pScopeList [in, out]

Pointer to a buffer used for storing scope list information, in the form of an 
<a href="https://msdn.microsoft.com/d275e78b-ddf3-4f92-a76f-463aec2f6c95">MCAST_SCOPE_ENTRY</a> structure. The return value of <i>pScopeList</i> depends on its input value, and on the value of the buffer to which it points: 




If <i>pScopeList</i> is a valid pointer on input, the scope list is returned.

If <i>pScopeList</i> is <b>NULL</b> on input, the length of the buffer required to hold the scope list is returned.

If the buffer pointed to in <i>pScopeList</i> is <b>NULL</b> on input, 
<b>McastEnumerateScopes</b> forces a repeat querying of scope lists from MCAST servers.

To determine the size of buffer required to hold scope list data, set <i>pScopeList</i> to <b>NULL</b> and <i>pScopeLen</i> to a non-<b>NULL</b> value. The 
<b>McastEnumerateScopes</b> function will then return ERROR_SUCCESS and store the size of the scope list data, in bytes, in <i>pScopeLen</i>.


### -param pScopeLen [in, out]

Pointer to a value used to communicate the size of data or buffer space in <i>pScopeList</i>. On input, <i>pScopeLen</i> points to the size, in bytes, of the buffer pointed to by <i>pScopeList</i>. On return, <i>pScopeLen</i> points to the size of the data copied to <i>pScopeList</i>. 




The <i>pScopeLen</i> parameter cannot be <b>NULL</b>. If the buffer pointed to by <i>pScopeList</i> is not large enough to hold the scope list data, 
<b>McastEnumerateScopes</b> returns ERROR_MORE_DATA and stores the required buffer size, in bytes, in <i>pScopeLen</i>.

To determine the size of buffer required to hold scope list data, set <i>pScopeList</i> to <b>NULL</b> and <i>pScopeLen</i> to a non-<b>NULL</b> value. The 
<b>McastEnumerateScopes</b> function will then return ERROR_SUCCESS and store the size of the scope list data, in bytes, in <i>pScopeLen</i>.


### -param pScopeCount [out]

Pointer to the number of scopes returned in <i>pScopeList</i>.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.

If the buffer pointed to by <i>pScopeList</i> is too small to hold the scope list, the 
<b>McastEnumerateScopes</b> function returns ERROR_MORE_DATA, and stores the required buffer size, in bytes, in <i>pScopeLen</i>.

If the 
<a href="https://msdn.microsoft.com/edb7d666-cbd0-46f7-b63e-2a09ffc9e9e2">McastApiStartup</a> function has not been called (it must be called before any other MADCAP client functions may be called), the 
<b>McastEnumerateScopes</b> function returns ERROR_NOT_READY.




## -remarks



The 
<b>McastEnumerateScopes</b> function queries multicast scopes for each network interface, and the interface on which the scope is retrieved is returned as part of the <i>pScopeList</i> parameter. Therefore, on multihomed computers it is possible that some scopes will get listed multiple times, once for each interface.




## -see-also




<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a>



<a href="https://msdn.microsoft.com/6460ea80-f1b1-4939-a977-580d0db10fd0">MCAST_CLIENT_UID</a>



<a href="https://msdn.microsoft.com/3110a1f3-e252-4eab-bf69-cbecfd65a5e0">MCAST_LEASE_REQUEST</a>



<a href="https://msdn.microsoft.com/1993e3bc-b6bd-4e13-aa71-7e33bf7ef540">MCAST_LEASE_RESPONSE</a>



<a href="https://msdn.microsoft.com/164d8f73-f5f5-4cc6-85ca-8e249192c202">MCAST_SCOPE_CTX</a>



<a href="https://msdn.microsoft.com/d275e78b-ddf3-4f92-a76f-463aec2f6c95">MCAST_SCOPE_ENTRY</a>



<a href="https://msdn.microsoft.com/eccf52ee-8145-4a8f-9d34-5a56bfc8a48c">McastApiCleanup</a>



<a href="https://msdn.microsoft.com/edb7d666-cbd0-46f7-b63e-2a09ffc9e9e2">McastApiStartup</a>



<a href="https://msdn.microsoft.com/67d5f149-d9b3-4903-a859-1ad33e310997">McastGenUID</a>



<a href="https://msdn.microsoft.com/6cb87e3b-0d2e-46f8-8ccf-6309c8fb888c">McastReleaseAddress</a>



<a href="https://msdn.microsoft.com/d1d26edb-f372-4d6d-a6e2-a8eeafadedc0">McastRenewAddress</a>



<a href="https://msdn.microsoft.com/856eb251-1909-41a1-8e4f-c081942280de">McastRequestAddress</a>
 

 

