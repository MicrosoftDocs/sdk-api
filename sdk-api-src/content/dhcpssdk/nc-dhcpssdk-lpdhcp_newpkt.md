---
UID: NC:dhcpssdk.LPDHCP_NEWPKT
title: LPDHCP_NEWPKT
author: windows-sdk-content
description: The DhcpNewPktHook function is called by Microsoft DHCP Server shortly after it receives a DHCP packet slated for processing.
old-location: dhcp\dhcpnewpkthook.htm
old-project: dhcp
ms.assetid: 2bff8750-aeb2-4164-9a6e-4239a6736beb
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: DhcpNewPktHook, DhcpNewPktHook callback function [DHCP], LPDHCP_NEWPKT, LPDHCP_NEWPKT callback, _dhcp_dhcpnewpkthook, dhcp.dhcpnewpkthook, dhcpssdk/DhcpNewPktHook
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: dhcpssdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: SCOPE_MIB_INFO_V5, *LPSCOPE_MIB_INFO_V5
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Dhcpssdk.h
api_name:
 - DhcpNewPktHook
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

