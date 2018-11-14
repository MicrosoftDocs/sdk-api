---
UID: NS:madcapcl._MCAST_CLIENT_UID
title: "_MCAST_CLIENT_UID"
author: windows-sdk-content
description: The MCAST_CLIENT_UID structure describes the unique client identifier for each multicast request.
old-location: madcap\mcast_client_uid.htm
tech.root: Madcap
ms.assetid: 6460ea80-f1b1-4939-a977-580d0db10fd0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPMCAST_CLIENT_UID, LPMCAST_CLIENT_UID, LPMCAST_CLIENT_UID structure pointer [MADCAP], MCAST_CLIENT_UID, MCAST_CLIENT_UID structure [MADCAP], _MCAST_CLIENT_UID, _mdhcp_mcast_client_uid, madcap.mcast_client_uid, madcapcl/LPMCAST_CLIENT_UID, madcapcl/MCAST_CLIENT_UID"
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
 - MCAST_CLIENT_UID
product: Windows
targetos: Windows
req.typenames: MCAST_CLIENT_UID, *LPMCAST_CLIENT_UID
req.redist: 
---

# _MCAST_CLIENT_UID structure


## -description


The 
<b>MCAST_CLIENT_UID</b> structure describes the unique client identifier for each multicast request.


## -struct-fields




### -field ClientUID

Buffer containing the unique client identifier.


### -field ClientUIDLength

Size of the <b>ClientUID</b> member, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/c3dc76aa-d903-49be-a4a2-1f66cafff40a">IPNG_ADDRESS</a>



<a href="https://msdn.microsoft.com/3110a1f3-e252-4eab-bf69-cbecfd65a5e0">MCAST_LEASE_REQUEST</a>



<a href="https://msdn.microsoft.com/164d8f73-f5f5-4cc6-85ca-8e249192c202">MCAST_SCOPE_CTX</a>



<a href="https://msdn.microsoft.com/d275e78b-ddf3-4f92-a76f-463aec2f6c95">MCAST_SCOPE_ENTRY</a>



<a href="https://msdn.microsoft.com/eccf52ee-8145-4a8f-9d34-5a56bfc8a48c">McastApiCleanup</a>



<a href="https://msdn.microsoft.com/edb7d666-cbd0-46f7-b63e-2a09ffc9e9e2">McastApiStartup</a>



<a href="https://msdn.microsoft.com/df33d766-d420-4069-8b94-86f5e4e91c1d">McastEnumerateScopes</a>



<a href="https://msdn.microsoft.com/67d5f149-d9b3-4903-a859-1ad33e310997">McastGenUID</a>



<a href="https://msdn.microsoft.com/856eb251-1909-41a1-8e4f-c081942280de">McastRequestAddress</a>
 

 

