---
UID: NS:dhcpsapi._DHCP_IP_RESERVATION_V4
title: DHCP_IP_RESERVATION_V4 (dhcpsapi.h)
description: The DHCP_IP_RESERVATION_V4 structure defines a client IP reservation. This structure extends an IP reservation by including the type of client (DHCP or BOOTP) holding the reservation.
helpviewer_keywords: ["*LPDHCP_IP_RESERVATION_V4","CLIENT_TYPE_BOOTP","CLIENT_TYPE_BOTH","CLIENT_TYPE_DHCP","DHCP_IP_RESERVATION_V4","DHCP_IP_RESERVATION_V4 structure [DHCP]","LPDHCP_IP_RESERVATION_V4","LPDHCP_IP_RESERVATION_V4 structure pointer [DHCP]","dhcp.dhcp_ip_reservation_v4","dhcpsapi/LPDHCP_IP_RESERVATION_V4","dhcpsapi/_DHCP_IP_RESERVATION_V4"]
old-location: dhcp\dhcp_ip_reservation_v4.htm
tech.root: DHCP
ms.assetid: 01951b18-fc54-4a34-9ccd-fd98f4e7864f
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_IP_RESERVATION_V4, CLIENT_TYPE_BOOTP, CLIENT_TYPE_BOTH, CLIENT_TYPE_DHCP, DHCP_IP_RESERVATION_V4, DHCP_IP_RESERVATION_V4 structure [DHCP], LPDHCP_IP_RESERVATION_V4, LPDHCP_IP_RESERVATION_V4 structure pointer [DHCP], dhcp.dhcp_ip_reservation_v4, dhcpsapi/LPDHCP_IP_RESERVATION_V4, dhcpsapi/_DHCP_IP_RESERVATION_V4'
req.header: dhcpsapi.h
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
req.typenames: DHCP_IP_RESERVATION_V4, *LPDHCP_IP_RESERVATION_V4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_IP_RESERVATION_V4
 - dhcpsapi/_DHCP_IP_RESERVATION_V4
 - LPDHCP_IP_RESERVATION_V4
 - dhcpsapi/LPDHCP_IP_RESERVATION_V4
 - DHCP_IP_RESERVATION_V4
 - dhcpsapi/DHCP_IP_RESERVATION_V4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_IP_RESERVATION_V4
---

# DHCP_IP_RESERVATION_V4 structure


## -description

The <b>DHCP_IP_RESERVATION_V4</b> structure defines a client IP reservation. This structure extends an IP reservation by including the type of client (DHCP or BOOTP) holding the reservation.

## -struct-fields

### -field ReservedIpAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the reserved IP address.

### -field ReservedForClient

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_CLIENT_UID</a> structure that contains the hardware address (MAC address) of the DHCPv4 client that holds this reservation.

### -field bAllowedClientTypes

Value that specifies the DHCPv4 reserved client type. The possible values are below:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_DHCP"></a><a id="client_type_dhcp"></a><dl>
<dt><b>CLIENT_TYPE_DHCP</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client supports the DHCP protocol only.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOOTP"></a><a id="client_type_bootp"></a><dl>
<dt><b>CLIENT_TYPE_BOOTP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client supports the BOOTP protocol only.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOTH"></a><a id="client_type_both"></a><dl>
<dt><b>CLIENT_TYPE_BOTH</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client supports both the DHCPv4 and the BOOTP protocols.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_reservation_info">DHCP_IP_RESERVATION_INFO</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_reservation_v6">DHCP_IP_RESERVATION_V6</a>