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

# tcp_request_query_information_ex_xp structure


## -description


<p class="CCE_Message">[This structure may be altered or unavailable in future versions of Windows.]

Contains the input for the <a href="https://msdn.microsoft.com/b992b585-e1c8-4262-a6e0-ad8b5047620f">IOCTL_TCP_QUERY_INFORMATION_EX</a> control code.


## -struct-fields




### -field ID

The <a href="https://msdn.microsoft.com/79d34f1c-2ea7-4867-9fb2-80401b0859bf">TDIObjectID</a> structure that defines the type of information being requested from the TCP driver by <a href="https://msdn.microsoft.com/b992b585-e1c8-4262-a6e0-ad8b5047620f">IOCTL_TCP_QUERY_INFORMATION_EX</a>.


### -field Context

The IPv4 or IPv6 address to be used when <a href="https://msdn.microsoft.com/dc9de369-f739-475c-96f5-e2e058705fe8">IPInterfaceInfo</a> data is requested for a particular IP address.


## -see-also




<a href="https://msdn.microsoft.com/b992b585-e1c8-4262-a6e0-ad8b5047620f">IOCTL_TCP_QUERY_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/dc9de369-f739-475c-96f5-e2e058705fe8">IPInterfaceInfo</a>



<a href="https://msdn.microsoft.com/79d34f1c-2ea7-4867-9fb2-80401b0859bf">TDIObjectID</a>
 

 

