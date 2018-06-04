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

# _WTS_SESSION_ADDRESS structure


## -description


Contains the virtual IP address assigned to a session. This structure is returned by the <a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a> function when you specify "WTSSessionAddressV4" for the <i>WTSInfoClass</i> parameter.


## -struct-fields




### -field AddressFamily

A null-terminated string that contains the address family. Always set this member to "AF_INET".


### -field Address

The virtual IP address assigned to the session. The format of this address is identical to that used in the <a href="https://msdn.microsoft.com/29034986-f8d1-4cf0-9f53-e4b195d450a6">WTS_CLIENT_ADDRESS</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>



<a href="https://msdn.microsoft.com/29034986-f8d1-4cf0-9f53-e4b195d450a6">WTS_CLIENT_ADDRESS</a>
 

 

