---
UID: NC:dhcpssdk.LPDHCP_GIVE_ADDRESS
title: LPDHCP_GIVE_ADDRESS
author: windows-sdk-content
description: The DhcpAddressOfferHook function is called by Microsoft DHCP Server directly before Microsoft DHCP Server sends an acknowledgement (ACK) to a DHCP REQUEST message.
old-location: dhcp\dhcpaddressofferhook.htm
tech.root: dhcp
ms.assetid: 1c122657-a92a-4232-879a-12105dc967e1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DHCP_CLIENT_BOOTP, DHCP_CLIENT_DHCP, DhcpAddressOfferHook, DhcpAddressOfferHook callback function [DHCP], LPDHCP_GIVE_ADDRESS, LPDHCP_GIVE_ADDRESS callback, _dhcp_dhcpaddressofferhook, dhcp.dhcpaddressofferhook, dhcpssdk/DhcpAddressOfferHook
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Dhcpssdk.h
api_name:
 - DhcpAddressOfferHook
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPDHCP_GIVE_ADDRESS callback function


## -description


The 
<b>DhcpAddressOfferHook</b> function is called by Microsoft DHCP Server directly before Microsoft DHCP Server sends an acknowledgement (ACK) to a DHCP REQUEST message. The 
<b>DhcpAddressOfferHook</b> is implemented by a third-party DLL that registers for notification of significant Microsoft DHCP Server events.

The 
<b>DhcpAddressOfferHook</b> function should not block.


## -parameters




### -param Packet [in]

Buffer for the packet being processed.


### -param PacketSize [in]

Size of the <i>Packet</i> parameter, in bytes.


### -param ControlCode [in]

Specifies the type of lease being approved. If the acknowledgement is for a new lease, <i>ControlCode</i> is DHCP_GIVE_ADDRESS_NEW. If the acknowledgement is for the renewal of an existing lease, <i>ControlCode</i> is DHCP_GIVE_ADDRESS_OLD.


### -param IpAddress [in]

Internet Protocol (IP) address of the socket on which the packet was received. The IP address is in host order.


### -param AltAddress [in]

Internet Protocol (IP) address being handed out in the lease.


### -param AddrType [in]

Specifies whether the address is a DHCP or BOOTP address. The default value is DHCP_CLIENT_DHCP.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_CLIENT_DHCP_"></a><a id="dhcp_client_dhcp_"></a><dl>
<dt><b>DHCP_CLIENT_DHCP </b></dt>
</dl>
</td>
<td width="60%">
The address is a DHCP-served address.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_CLIENT_BOOTP_"></a><a id="dhcp_client_bootp_"></a><dl>
<dt><b>DHCP_CLIENT_BOOTP </b></dt>
</dl>
</td>
<td width="60%">
The address is a BOOTP-served address.

</td>
</tr>
</table>
 


### -param LeaseTime [in]

Lease duration being passed, in seconds.


### -param Reserved [in]

Reserve for future use.


### -param PktContext [in]

Context identifying the packet, as provided in the <i>PktContext</i> parameter of a previous 
<a href="https://msdn.microsoft.com/2bff8750-aeb2-4164-9a6e-4239a6736beb">DhcpNewPktHook</a> function call.


## -returns



Return values are defined by the application providing the callback.




## -remarks



Implementations of the 
<b>DhcpAddressOfferHook</b> should not block.




## -see-also




<a href="https://msdn.microsoft.com/fa57e5c5-2335-44ba-8642-61dcb8b33ffe">DHCP_CALLOUT_TABLE</a>



<a href="https://msdn.microsoft.com/2bff8750-aeb2-4164-9a6e-4239a6736beb">DhcpNewPktHook</a>
 

 

