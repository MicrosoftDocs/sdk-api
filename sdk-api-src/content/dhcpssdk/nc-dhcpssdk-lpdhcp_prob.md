---
UID: NC:dhcpssdk.LPDHCP_PROB
title: LPDHCP_PROB
author: windows-sdk-content
description: The DhcpAddressDelHook function is called by Microsoft DHCP Server when one of the following four defined events occurs.
old-location: dhcp\dhcpaddressdelhook.htm
tech.root: DHCP
ms.assetid: fd9ce5df-927d-4b34-9561-ff5a2ebad16e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpAddressDelHook, DhcpAddressDelHook callback function [DHCP], LPDHCP_PROB, LPDHCP_PROB callback, _dhcp_dhcpaddressdelhook, dhcp.dhcpaddressdelhook, dhcpssdk/DhcpAddressDelHook
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
 - DhcpAddressDelHook
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPDHCP_PROB callback function


## -description


The 
<b>DhcpAddressDelHook</b> function is called by Microsoft DHCP Server when one of the following four defined events occurs:
<ul>
<li>DHCP_PROB_CONFLICT</li>
<li>DHCP_PROB_DECLINE</li>
<li>DHCP_PROB_RELEASE</li>
<li>DHCP_PROB_NACKED</li>
</ul>See Remarks for more information on these events. The 
<b>DhcpAddressDelHook</b> function is implemented by a third-party DLL that registers for notification of significant Microsoft DHCP Server events. The 
<b>DhcpAddressDelHook</b> function should not block.


## -parameters




### -param Packet [in]

Buffer for the packet being processed.


### -param PacketSize [in]

Size of the <i>Packet</i> parameter, in bytes.


### -param ControlCode [in]

Specifies the event. See Remarks for control code definitions.


### -param IpAddress [in]

Internet Protocol (IP) address of the socket on which the packet was received. The IP address is in host order.


### -param AltAddress [in]

Internet Protocol (IP) address used to provide additional information about the event. The meaning of <i>AltAddress</i> varies based on the value of <i>ControlCode</i>. See Remarks.


### -param Reserved [in]

Reserve for future use.


### -param PktContext [in]

Context identifying the packet, as provided in the <i>PktContext</i> parameter of a previous 
<a href="https://msdn.microsoft.com/2bff8750-aeb2-4164-9a6e-4239a6736beb">DhcpNewPktHook</a> function call.


## -returns



Return values are defined by the application providing the callback.




## -remarks



The following table defines the four defined events that trigger Microsoft DHCP Server to call the 
<b>DhcpAddressDelHook</b> function in a third-party DLL.

<table>
<tr>
<th>Control code</th>
<th>Description</th>
</tr>
<tr>
<td>DHCP_PROB_CONFLICT</td>
<td>The address attempted to be offered, as provided in <i>AltAddress</i>, is already in use on the network.</td>
</tr>
<tr>
<td>DHCP_PROB_DECLINE</td>
<td>The packet was a DECLINE message for the address specified in <i>AltAddress</i>.</td>
</tr>
<tr>
<td>DHCP_PROB_RELEASE</td>
<td>The packet was a RELEASE message for the address specified in <i>AltAddress</i>.</td>
</tr>
<tr>
<td>DHCP_PROB_NACKED</td>
<td>The packet was a REQUEST message for the address specified in <i>AltAddress</i>, and the request was declined by Microsoft DHCP Server.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fa57e5c5-2335-44ba-8642-61dcb8b33ffe">DHCP_CALLOUT_TABLE</a>



<a href="https://msdn.microsoft.com/2bff8750-aeb2-4164-9a6e-4239a6736beb">DhcpNewPktHook</a>
 

 

