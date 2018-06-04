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

# LPDHCP_NEWPKT callback function


## -description


The 
<b>DhcpNewPktHook</b> function is called by Microsoft DHCP Server shortly after it receives a DHCP packet slated for processing. Since the 
<b>DhcpNewPktHook</b> function call is in the critical path for Microsoft DHCP Server processing, this function should execute and return as quickly as possible or performance will be impacted.

The 
<b>DhcpNewPktHook</b> function is implemented by a third-party DLL that registers for notification of significant Microsoft DHCP Server events.


## -parameters




### -param *Packet [in, out]

Pointer to a 4Kb character buffer that contains the packet.

<div class="alert"><b>Note</b>  Writing to this buffer directly is not recommended.</div>
<div> </div>

### -param *PacketSize [in, out]

Pointer to the size of the <i>Packet</i> parameter.


### -param IpAddress [in]

Pointer to the IP address of the socket on which the packet was received. The IP address is in host order.


### -param Reserved [in]

Reserved for future use.


### -param *PktContext [in, out]

Pointer provided by the third-party DLL, and used by Microsoft DHCP Server in future references to this specific packet. Third-party DLLs interested in such tracking are responsible for providing and tracking this packet context.


### -param ProcessIt [out]

Flag identifying whether Microsoft DHCP Server should continue processing the packet. Set to <b>TRUE</b> to indicate processing should proceed. Set to <b>FALSE</b> to have Microsoft DHCP Server drop the packet.


## -returns



Return values are defined by the application providing the callback.




## -remarks



If useful, third-party DLLs can modify the <i>Packet</i> buffer, or return a new packet buffer through appropriate modification of the <i>Packet</i> and <i>PacketSize</i> parameters.

If a third-party DLL needs to keep track of a given packet and its progress through Microsoft DHCP Server, it can provide a packet context in <i>PktContext</i>, and use internal structures that track the packet's progress through its DHCP processing. A context provided in <i>PktContext</i> will be passed as a parameter to many other DHCP Server API functions, enabling identification.




## -see-also




<a href="https://msdn.microsoft.com/fa57e5c5-2335-44ba-8642-61dcb8b33ffe">DHCP_CALLOUT_TABLE</a>



<a href="https://msdn.microsoft.com/a80c2cd3-291d-4646-9dba-20a42e78dee5">DhcpServerCalloutEntry</a>



<a href="https://msdn.microsoft.com/35ec953e-0345-4c18-8790-33da189c6a43">How the
		  DHCP Server API Operates</a>
 

 

