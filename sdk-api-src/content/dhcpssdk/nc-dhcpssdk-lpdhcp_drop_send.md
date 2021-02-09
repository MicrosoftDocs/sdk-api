---
UID: NC:dhcpssdk.LPDHCP_DROP_SEND
title: LPDHCP_DROP_SEND (dhcpssdk.h)
description: LPDHCP_DROP_SEND callback function
helpviewer_keywords: ["DhcpPktDropHook","DhcpPktSendHook","LPDHCP_DROP_SEND","LPDHCP_DROP_SEND callback","LPDHCP_DROP_SEND callback function [DHCP]","_dhcp_dhcppktdrophook","dhcp.dhcppktdrophook","dhcpssdk/LPDHCP_DROP_SEND"]
old-location: dhcp\dhcppktdrophook.htm
tech.root: DHCP
ms.assetid: 29fa3266-a0a7-4e17-bf15-35a454f78b12
ms.date: 12/05/2018
ms.keywords: DhcpPktDropHook, DhcpPktSendHook, LPDHCP_DROP_SEND, LPDHCP_DROP_SEND callback, LPDHCP_DROP_SEND callback function [DHCP], _dhcp_dhcppktdrophook, dhcp.dhcppktdrophook, dhcpssdk/LPDHCP_DROP_SEND
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPDHCP_DROP_SEND
 - dhcpssdk/LPDHCP_DROP_SEND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Dhcpssdk.h
api_name:
 - LPDHCP_DROP_SEND
---

# LPDHCP_DROP_SEND callback function


## -description

## -parameters

### -param Packet [in, out]

Pointer to a buffer, 4Kb in size,  that contains the packet.

<div class="alert"><b>Note</b>  Writing to this buffer directly is not recommended.</div>
<div> </div>

### -param PacketSize [in, out]

Pointer to the size of the <i>Packet</i> parameter, in bytes.

### -param ControlCode [in]

Control code that specifies the reason for dropping. See Remarks.

### -param IpAddress [in]

Internet Protocol (IP) address of the socket on which the packet was received. The IP address is in host order.

### -param Reserved [in]

Reserved for future use.

### -param PktContext [in]

Context identifying the packet, as provided in the <i>PktContext</i> parameter of a previous 
<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_newpkt">DhcpNewPktHook</a> function call.

## -returns

Return values are defined by the application providing the callback.

## -remarks

The 
<b>DhcpPktDropHook</b> function is called by Microsoft DHCP Server when a DHCP packet is dropped, or a packet is completely processed. The 
<b>DhcpPktDropHook</b> is implemented by a third-party DLL that registers for notification of significant Microsoft DHCP Server events.

The 
<b>DhcpPktDropHook</b> function should not block.

Third-party DLLs that register for notification of this event should be prepared to have their 
<b>DhcpPktDropHook</b> function called multiple times for each packet. If a packet is dropped by Microsoft DHCP Server, this function is called twice for that packet: once to notify that the packet was dropped, and again to identify that the packet was completely processed.

The following table defines the possible control codes returned in the <i>ControlCode</i> parameter.

<table>
<tr>
<th>Control code</th>
<th>Description</th>
</tr>
<tr>
<td>DHCP_DROP_DUPLICATE</td>
<td>The packet is a duplicate of another received by the DHCP server.</td>
</tr>
<tr>
<td>DHCP_DROP_NOMEM</td>
<td>There is not enough memory available to process the packet.</td>
</tr>
<tr>
<td>DHCP_DROP_INTERNAL_ERROR</td>
<td>An unexpected internal error has occurred.</td>
</tr>
<tr>
<td>DHCP_DROP_TIMEOUT</td>
<td>The packet is too old to process.</td>
</tr>
<tr>
<td>DHCP_DROP_UNAUTH</td>
<td>The server is not authorized to process this packet.</td>
</tr>
<tr>
<td>DHCP_DROP_PAUSED</td>
<td>The server is paused.</td>
</tr>
<tr>
<td>DHCP_DROP_NO_SUBNETS</td>
<td>There are no subnets configured, therefore there is no point in processing the packet.</td>
</tr>
<tr>
<td>DHCP_DROP_INVALID</td>
<td>The packet is invalid, or it was received on an invalid socket.</td>
</tr>
<tr>
<td>DHCP_DROP_WRONG_SERVER</td>
<td>The packet was sent to the wrong DHCP Server.</td>
</tr>
<tr>
<td>DHCP_DROP_NOADDRESS</td>
<td>There is no address to offer.</td>
</tr>
<tr>
<td>DHCP_DROP_PROCESSED</td>
<td>The packet has been processed.</td>
</tr>
<tr>
<td>DHCP_DROP_GEN_FAILURE</td>
<td>An unknown error has occurred.</td>
</tr>
</table>
 

The 
<b>DhcpPktSendHook</b> function is called by Microsoft DHCP Server directly before Microsoft DHCP Server sends a response to a client. Registering for notification of 
<b>DhcpPktSendHook</b> enables third-party developers to alter the response of the Microsoft DHCP Server by manipulation of the packet pointers. The 
<b>DhcpPktSendHook</b> is implemented by a third-party DLL that registers for notification of significant Microsoft DHCP Server events.

The 
<b>DhcpPktSendHook</b> function should not block.

The 
<b>DhcpPktSendHook</b> function should not block.

## -see-also

<a href="/windows/desktop/api/dhcpssdk/ns-dhcpssdk-dhcp_callout_table">DHCP_CALLOUT_TABLE</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_newpkt">DhcpNewPktHook</a>
