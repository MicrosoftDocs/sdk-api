---
UID: NC:dhcpssdk.LPDHCP_NEWPKT
title: LPDHCP_NEWPKT (dhcpssdk.h)
description: The DhcpNewPktHook function is called by Microsoft DHCP Server shortly after it receives a DHCP packet slated for processing.
helpviewer_keywords: ["DhcpNewPktHook","DhcpNewPktHook callback function [DHCP]","LPDHCP_NEWPKT","LPDHCP_NEWPKT callback","_dhcp_dhcpnewpkthook","dhcp.dhcpnewpkthook","dhcpssdk/DhcpNewPktHook"]
old-location: dhcp\dhcpnewpkthook.htm
tech.root: DHCP
ms.assetid: 2bff8750-aeb2-4164-9a6e-4239a6736beb
ms.date: 12/05/2018
ms.keywords: DhcpNewPktHook, DhcpNewPktHook callback function [DHCP], LPDHCP_NEWPKT, LPDHCP_NEWPKT callback, _dhcp_dhcpnewpkthook, dhcp.dhcpnewpkthook, dhcpssdk/DhcpNewPktHook
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
 - LPDHCP_NEWPKT
 - dhcpssdk/LPDHCP_NEWPKT
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
 - DhcpNewPktHook
---

# LPDHCP_NEWPKT callback function


## -description

The 
<b>DhcpNewPktHook</b> function is called by Microsoft DHCP Server shortly after it receives a DHCP packet slated for processing. Since the 
<b>DhcpNewPktHook</b> function call is in the critical path for Microsoft DHCP Server processing, this function should execute and return as quickly as possible or performance will be impacted.

The 
<b>DhcpNewPktHook</b> function is implemented by a third-party DLL that registers for notification of significant Microsoft DHCP Server events.

## -parameters

### -param Packet [in, out]

Pointer to a 4Kb character buffer that contains the packet.

<div class="alert"><b>Note</b>  Writing to this buffer directly is not recommended.</div>
<div> </div>

### -param PacketSize [in, out]

Pointer to the size of the <i>Packet</i> parameter.

### -param IpAddress [in]

Pointer to the IP address of the socket on which the packet was received. The IP address is in host order.

### -param Reserved [in]

Reserved for future use.

### -param PktContext [in, out]

Pointer provided by the third-party DLL, and used by Microsoft DHCP Server in future references to this specific packet. Third-party DLLs interested in such tracking are responsible for providing and tracking this packet context.

### -param ProcessIt [out]

Flag identifying whether Microsoft DHCP Server should continue processing the packet. Set to <b>TRUE</b> to indicate processing should proceed. Set to <b>FALSE</b> to have Microsoft DHCP Server drop the packet.

## -returns

Return values are defined by the application providing the callback.

## -remarks

If useful, third-party DLLs can modify the <i>Packet</i> buffer, or return a new packet buffer through appropriate modification of the <i>Packet</i> and <i>PacketSize</i> parameters.

If a third-party DLL needs to keep track of a given packet and its progress through Microsoft DHCP Server, it can provide a packet context in <i>PktContext</i>, and use internal structures that track the packet's progress through its DHCP processing. A context provided in <i>PktContext</i> will be passed as a parameter to many other DHCP Server API functions, enabling identification.

## -see-also

<a href="/windows/desktop/api/dhcpssdk/ns-dhcpssdk-dhcp_callout_table">DHCP_CALLOUT_TABLE</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_entry_point_func">DhcpServerCalloutEntry</a>



<a href="/previous-versions/windows/desktop/dhcp/how-the-dhcp-server-api-operates">How the
		  DHCP Server API Operates</a>
