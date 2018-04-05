---
UID: NF:madcapcl.McastGenUID
title: McastGenUID function
author: windows-driver-content
description: The McastGenUID function generates a unique identifier, subsequently used by clients to request and renew addresses.
old-location: madcap\mcastgenuid.htm
old-project: Madcap
ms.assetid: 67d5f149-d9b3-4903-a859-1ad33e310997
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: McastGenUID, McastGenUID function [MADCAP], _mdhcp_mcastgenuid, madcap.mcastgenuid, madcapcl/McastGenUID
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
req.typenames: POLICY_DNS_DOMAIN_INFO, *PPOLICY_DNS_DOMAIN_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpcsvc.dll
api_name:
-	McastGenUID
product: Windows
targetos: Windows
req.lib: Dhcpcsvc.lib
req.dll: Dhcpcsvc.dll
req.irql: 
req.product: GDI+ 1.1
---

# McastGenUID function


## -description


The 
<b>McastGenUID</b> function generates a unique identifier, subsequently used by clients to request and renew addresses.


## -parameters




### -param pRequestID [in]

Pointer to the 
<a href="https://msdn.microsoft.com/6460ea80-f1b1-4939-a977-580d0db10fd0">MCAST_CLIENT_UID</a> structure into which the unique identifier is stored. The size of the buffer to which <i>pRequestID</i> points must be at least MCAST_CLIENT_ID_LEN in size.


## -returns



The 
<b>McastGenUID</b> function returns the status of the operation.




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



<a href="https://msdn.microsoft.com/6cb87e3b-0d2e-46f8-8ccf-6309c8fb888c">McastReleaseAddress</a>



<a href="https://msdn.microsoft.com/d1d26edb-f372-4d6d-a6e2-a8eeafadedc0">McastRenewAddress</a>



<a href="https://msdn.microsoft.com/856eb251-1909-41a1-8e4f-c081942280de">McastRequestAddress</a>
 

 

