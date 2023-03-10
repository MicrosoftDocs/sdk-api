---
UID: NS:dhcpssdk._DHCP_CALLOUT_TABLE
title: DHCP_CALLOUT_TABLE (dhcpssdk.h)
description: The DHCP_CALLOUT_TABLE structure is used by Microsoft DHCP Server and third-party DLLs to send notification requests for DHCP Server events.
helpviewer_keywords: ["*LPDHCP_CALLOUT_TABLE","DHCP_CALLOUT_TABLE","DHCP_CALLOUT_TABLE structure [DHCP]","LPDHCP_CALLOUT_TABLE","LPDHCP_CALLOUT_TABLE structure pointer [DHCP]","_dhcp_dhcp_callout_table","dhcp.dhcp_callout_table","dhcpssdk/DHCP_CALLOUT_TABLE","dhcpssdk/LPDHCP_CALLOUT_TABLE"]
old-location: dhcp\dhcp_callout_table.htm
tech.root: DHCP
ms.assetid: fa57e5c5-2335-44ba-8642-61dcb8b33ffe
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CALLOUT_TABLE, DHCP_CALLOUT_TABLE, DHCP_CALLOUT_TABLE structure [DHCP], LPDHCP_CALLOUT_TABLE, LPDHCP_CALLOUT_TABLE structure pointer [DHCP], _dhcp_dhcp_callout_table, dhcp.dhcp_callout_table, dhcpssdk/DHCP_CALLOUT_TABLE, dhcpssdk/LPDHCP_CALLOUT_TABLE'
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
req.typenames: DHCP_CALLOUT_TABLE, *LPDHCP_CALLOUT_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CALLOUT_TABLE
 - dhcpssdk/_DHCP_CALLOUT_TABLE
 - LPDHCP_CALLOUT_TABLE
 - dhcpssdk/LPDHCP_CALLOUT_TABLE
 - DHCP_CALLOUT_TABLE
 - dhcpssdk/DHCP_CALLOUT_TABLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpssdk.h
api_name:
 - DHCP_CALLOUT_TABLE
---

# DHCP_CALLOUT_TABLE structure


## -description

The 
<b>DHCP_CALLOUT_TABLE</b> structure is used by Microsoft DHCP Server and third-party DLLs to send notification requests for DHCP Server events.

## -struct-fields

### -field DhcpControlHook

Pointer to a 
<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_control">DhcpControlHook</a> function, implemented in a third-party DLL, to be called when Microsoft DHCP Server is started, stopped, paused, or continued. Set to <b>NULL</b> if notification is not required.

### -field DhcpNewPktHook

Pointer to a 
<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_newpkt">DhcpNewPktHook</a> function, implemented in a third-party DLL, to be called when Microsoft DHCP Server receives a packet that it attempts to process. Set to <b>NULL</b> if notification is not required.

### -field DhcpPktDropHook

Pointer to a 
<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_drop_send">DhcpPktDropHook</a> function, implemented in a third-party DLL, to be called when Microsoft DHCP Server drops a packet, and when a packet is completely processed by Microsoft DHCP Server. Set to <b>NULL</b> if notification is not required.

### -field DhcpPktSendHook

Pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa363294(v=vs.85)">DhcpPktSendHook</a> function, implemented in a third-party DLL, to be called directly before Microsoft DHCP Server submits a response to a client inquiry. Set to <b>NULL</b> if notification is not required.

### -field DhcpAddressDelHook

Pointer to a 
<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_prob">DhcpAddressDelHook</a> function, implemented in a third-party DLL, to be called when a specified event in Microsoft DHCP Server results in a packet being dropped. Set to <b>NULL</b> if notification is not required.

### -field DhcpAddressOfferHook

Pointer to a 
<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_give_address">DhcpAddressOfferHook</a> function, implemented in a third-party DLL, to be called directly before Microsoft DHCP Server submits a DHCP ACK message in response to a DHCP REQUEST message. Set to <b>NULL</b> if notification is not required.

### -field DhcpHandleOptionsHook

Pointer to a 
<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_handle_options">DhcpHandleOptionsHook</a> function, implemented in a third-party DLL, that sends only parsed DHCP information to the third-party DLL, enabling the third-party DLL to avoid processing the entire DHCP packet. Set to <b>NULL</b> if notification is not required.

### -field DhcpDeleteClientHook

Pointer to a 
<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_delete_client">DhcpDeleteClientHook</a> function, implemented in a third-party DLL, to be called directly before Microsoft DHCP Server deletes a client lease from its active leases database. Set to <b>NULL</b> if notification is not required.

### -field DhcpExtensionHook

Reserved for future use.

### -field DhcpReservedHook

Reserved for future use.

## -remarks

It is not necessary to implement all hooks available from Microsoft DHCP Server. If notification for a particular event is not required, set the member to <b>NULL</b>. Remember, however, that the initially loaded third-party DLL is responsible for loading subsequent third-party DLLs, and that subsequent DLLs may require notification of events that otherwise would be <b>NULL</b>, resulting in a non-<b>NULL</b> setting for members used by chained third-party DLLs that would otherwise be unused.

## -see-also

<a href="/previous-versions/windows/desktop/dhcp/chaining-multiple-third-party-dlls">Chaining Multiple Third-Party DLLs</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_prob">DhcpAddressDelHook</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_give_address">DhcpAddressOfferHook</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_control">DhcpControlHook</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_delete_client">DhcpDeleteClientHook</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_handle_options">DhcpHandleOptionsHook</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_newpkt">DhcpNewPktHook</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_drop_send">DhcpPktDropHook</a>



<a href="/previous-versions/windows/desktop/legacy/aa363294(v=vs.85)">DhcpPktSendHook</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_entry_point_func">DhcpServerCalloutEntry</a>