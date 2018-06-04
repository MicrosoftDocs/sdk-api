---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DhcpCApiInitialize function


## -description


The 
<b>DhcpCApiInitialize</b> function must be the first function call made by users of DHCP; it prepares the system for all other DHCP function calls. Other DHCP functions should only be called if the 
<b>DhcpCApiInitialize</b> function executes successfully.


## -parameters




### -param Version [out]

Pointer to the DHCP version implemented by the client.


## -returns



Returns ERROR_SUCCESS upon successful completion.




## -see-also




<a href="https://msdn.microsoft.com/ca859a72-51d3-4bd5-96b9-7a9a2df95595">DHCP Functions</a>



<a href="https://msdn.microsoft.com/c1da731c-2e06-40ae-b104-25f144d50c36">DhcpCApiCleanup</a>
 

 

