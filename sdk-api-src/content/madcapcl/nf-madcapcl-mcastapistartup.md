---
UID: NF:madcapcl.McastApiStartup
title: McastApiStartup function
author: windows-sdk-content
description: The McastApiStartup function facilitates MADCAP-version negotiation between requesting clients and the version of MADCAP implemented on the system.
old-location: madcap\mcastapistartup.htm
tech.root: Madcap
ms.assetid: edb7d666-cbd0-46f7-b63e-2a09ffc9e9e2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: McastApiStartup, McastApiStartup function [MADCAP], _mdhcp_mcastapistartup, madcap.mcastapistartup, madcapcl/McastApiStartup
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
 - McastApiStartup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a>



<a href="https://msdn.microsoft.com/6460ea80-f1b1-4939-a977-580d0db10fd0">MCAST_CLIENT_UID</a>



<a href="https://msdn.microsoft.com/3110a1f3-e252-4eab-bf69-cbecfd65a5e0">MCAST_LEASE_REQUEST</a>



<a href="https://msdn.microsoft.com/1993e3bc-b6bd-4e13-aa71-7e33bf7ef540">MCAST_LEASE_RESPONSE</a>



<a href="https://msdn.microsoft.com/164d8f73-f5f5-4cc6-85ca-8e249192c202">MCAST_SCOPE_CTX</a>



<a href="https://msdn.microsoft.com/d275e78b-ddf3-4f92-a76f-463aec2f6c95">MCAST_SCOPE_ENTRY</a>



<a href="https://msdn.microsoft.com/eccf52ee-8145-4a8f-9d34-5a56bfc8a48c">McastApiCleanup</a>



<a href="https://msdn.microsoft.com/df33d766-d420-4069-8b94-86f5e4e91c1d">McastEnumerateScopes</a>



<a href="https://msdn.microsoft.com/67d5f149-d9b3-4903-a859-1ad33e310997">McastGenUID</a>



<a href="https://msdn.microsoft.com/6cb87e3b-0d2e-46f8-8ccf-6309c8fb888c">McastReleaseAddress</a>



<a href="https://msdn.microsoft.com/d1d26edb-f372-4d6d-a6e2-a8eeafadedc0">McastRenewAddress</a>



<a href="https://msdn.microsoft.com/856eb251-1909-41a1-8e4f-c081942280de">McastRequestAddress</a>
 

 

