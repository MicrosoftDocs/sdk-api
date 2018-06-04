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

# LPDHCP_DELETE_CLIENT callback function


## -description


The 
<b>DhcpDeleteClientHook</b> function is called by Microsoft DHCP Server directly before a client lease is deleted from the active leases database.

The 
<b>DhcpDeleteClientHook</b> function should not block.


## -parameters




### -param IpAddress [in]

Internet Protocol (IP) address of the client lease being deleted. The IP address is in host order.


### -param HwAddress [in]

Buffer holding the Hardware address of the client, often referred to as the MAC address.


### -param HwAddressLength [in]

Length of the <i>HwAddress</i> buffer, in bytes.


### -param Reserved [in]

Reserved for future use.


### -param ClientType [in]

Reserved for future use.


## -returns



Return values are defined by the application providing the callback.




## -remarks



The 
<b>DhcpDeleteClientHook</b> function should not block.




## -see-also




<a href="https://msdn.microsoft.com/fa57e5c5-2335-44ba-8642-61dcb8b33ffe">DHCP_CALLOUT_TABLE</a>
 

 

