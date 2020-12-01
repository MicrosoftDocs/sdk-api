---
UID: NC:dhcpssdk.LPDHCP_HANDLE_OPTIONS
title: LPDHCP_HANDLE_OPTIONS (dhcpssdk.h)
description: The DhcpHandleOptionsHook function enables third-party DLLs to obtain commonly used options from a DHCP packet, avoiding the need to process the entire DHCP packet. The DhcpHandleOptionsHook function should not block.
helpviewer_keywords: ["DhcpHandleOptionsHook","DhcpHandleOptionsHook callback function [DHCP]","LPDHCP_HANDLE_OPTIONS","LPDHCP_HANDLE_OPTIONS callback","_dhcp_dhcphandleoptionshook","dhcp.dhcphandleoptionshook","dhcpssdk/DhcpHandleOptionsHook"]
old-location: dhcp\dhcphandleoptionshook.htm
tech.root: DHCP
ms.assetid: 51bb3d2c-953d-446a-ad70-eb6cc8d4dbca
ms.date: 12/05/2018
ms.keywords: DhcpHandleOptionsHook, DhcpHandleOptionsHook callback function [DHCP], LPDHCP_HANDLE_OPTIONS, LPDHCP_HANDLE_OPTIONS callback, _dhcp_dhcphandleoptionshook, dhcp.dhcphandleoptionshook, dhcpssdk/DhcpHandleOptionsHook
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
 - LPDHCP_HANDLE_OPTIONS
 - dhcpssdk/LPDHCP_HANDLE_OPTIONS
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
 - DhcpHandleOptionsHook
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
<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_newpkt">DhcpNewPktHook</a> function call.

### -param ServerOptions [in, out]

Structure of type <a href="/windows/desktop/api/dhcpssdk/ns-dhcpssdk-dhcp_server_options">DHCP_SERVER_OPTIONS</a> containing the information parsed from the packet by Microsoft DHCP Server, and provided as the collection of commonly used server options.

## -returns

Return values are defined by the application providing the callback.

## -remarks

The 
<i>DhcpHandleOptionsHook</i> function is useful when developers of third-party DLLs want to avoid having to process an entire DHCP packet, and rather, could achieve the desired results by a set of commonly used server options. When third-party DLLs register for this event notification, the Microsoft DHCP Server parses the incoming packet, extracts commonly used server options, and passes them to the third-party DLL in the <i>ServerOptions</i> parameter.

If the <a href="/windows/desktop/api/dhcpssdk/ns-dhcpssdk-dhcp_server_options">DHCP_SERVER_OPTIONS</a> structure pointed to in <i>ServerOptions</i> is needed beyond the completion of the 
<i>DhcpHandleOptionsHook</i> function call, third-party DLLs must make a copy of the structure.

The 
<i>DhcpHandleOptionsHook</i> function can be called multiple times for a single packet.

## -see-also

<a href="/windows/desktop/api/dhcpssdk/ns-dhcpssdk-dhcp_callout_table">DHCP_CALLOUT_TABLE</a>



<a href="/windows/desktop/api/dhcpssdk/ns-dhcpssdk-dhcp_server_options">DHCP_SERVER_OPTIONS</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_newpkt">DhcpNewPktHook</a>