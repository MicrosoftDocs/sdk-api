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

# LPDHCP_HANDLE_OPTIONS callback function


## -description


The 
<i>DhcpHandleOptionsHook</i> function enables third-party DLLs to obtain commonly used options from a DHCP packet, avoiding the need to process the entire DHCP packet. The 
<i>DhcpHandleOptionsHook</i> function should not block.


## -parameters




### -param Packet [in]

Buffer for the packet being processed.


### -param PacketSize [in]

Size of the <i>Packet</i> parameter, in bytes.


### -param Reserved [in]

Reserve for future use.


### -param PktContext [in]

Context identifying the packet, as provided in the <i>PktContext</i> parameter of a previous 
<a href="https://msdn.microsoft.com/2bff8750-aeb2-4164-9a6e-4239a6736beb">DhcpNewPktHook</a> function call.


### -param ServerOptions [in, out]

Structure of type <a href="https://msdn.microsoft.com/0c43c2ad-ac9a-43b4-b750-a3f52c025ae2">DHCP_SERVER_OPTIONS</a> containing the information parsed from the packet by Microsoft DHCP Server, and provided as the collection of commonly used server options.


## -returns



Return values are defined by the application providing the callback.




## -remarks



The 
<i>DhcpHandleOptionsHook</i> function is useful when developers of third-party DLLs want to avoid having to process an entire DHCP packet, and rather, could achieve the desired results by a set of commonly used server options. When third-party DLLs register for this event notification, the Microsoft DHCP Server parses the incoming packet, extracts commonly used server options, and passes them to the third-party DLL in the <i>ServerOptions</i> parameter.

If the <a href="https://msdn.microsoft.com/0c43c2ad-ac9a-43b4-b750-a3f52c025ae2">DHCP_SERVER_OPTIONS</a> structure pointed to in <i>ServerOptions</i> is needed beyond the completion of the 
<i>DhcpHandleOptionsHook</i> function call, third-party DLLs must make a copy of the structure.

The 
<i>DhcpHandleOptionsHook</i> function can be called multiple times for a single packet.




## -see-also




<a href="https://msdn.microsoft.com/fa57e5c5-2335-44ba-8642-61dcb8b33ffe">DHCP_CALLOUT_TABLE</a>



<a href="https://msdn.microsoft.com/0c43c2ad-ac9a-43b4-b750-a3f52c025ae2">DHCP_SERVER_OPTIONS</a>



<a href="https://msdn.microsoft.com/2bff8750-aeb2-4164-9a6e-4239a6736beb">DhcpNewPktHook</a>
 

 

