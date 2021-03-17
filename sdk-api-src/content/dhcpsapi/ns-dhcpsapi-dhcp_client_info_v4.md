---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_V4
title: DHCP_CLIENT_INFO_V4 (dhcpsapi.h)
description: Defines a client information record used by the DHCP server, extending the definition provided in DHCP_CLIENT_INFO by including client type information.
helpviewer_keywords: ["*LPDHCP_CLIENT_INFO_V4","CLIENT_TYPE_BOOTP","CLIENT_TYPE_BOTH","CLIENT_TYPE_DHCP","CLIENT_TYPE_NONE","CLIENT_TYPE_UNSPECIFIED","DHCP_CLIENT_INFO_V4","DHCP_CLIENT_INFO_V4 structure [DHCP]","LPDHCP_CLIENT_INFO_V4","LPDHCP_CLIENT_INFO_V4 structure pointer [DHCP]","dhcp.dhcp_client_info_v4","dhcpsapi/LPDHCP_CLIENT_INFO_V4","dhcpsapi/_DHCP_CLIENT_INFO_V4"]
old-location: dhcp\dhcp_client_info_v4.htm
tech.root: DHCP
ms.assetid: ac058d7a-7257-4e40-8fc0-bc4ca107671b
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLIENT_INFO_V4, CLIENT_TYPE_BOOTP, CLIENT_TYPE_BOTH, CLIENT_TYPE_DHCP, CLIENT_TYPE_NONE, CLIENT_TYPE_UNSPECIFIED, DHCP_CLIENT_INFO_V4, DHCP_CLIENT_INFO_V4 structure [DHCP], LPDHCP_CLIENT_INFO_V4, LPDHCP_CLIENT_INFO_V4 structure pointer [DHCP], dhcp.dhcp_client_info_v4, dhcpsapi/LPDHCP_CLIENT_INFO_V4, dhcpsapi/_DHCP_CLIENT_INFO_V4'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DHCP_CLIENT_INFO_V4, *LPDHCP_CLIENT_INFO_V4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLIENT_INFO_V4
 - dhcpsapi/_DHCP_CLIENT_INFO_V4
 - LPDHCP_CLIENT_INFO_V4
 - dhcpsapi/LPDHCP_CLIENT_INFO_V4
 - DHCP_CLIENT_INFO_V4
 - dhcpsapi/DHCP_CLIENT_INFO_V4
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
 - DHCP_CLIENT_INFO_V4
---

# DHCP_CLIENT_INFO_V4 structure


## -description

The <b>DHCP_CLIENT_INFO_V4</b> structure defines a client information record used by the DHCP server, extending the definition provided in <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info">DHCP_CLIENT_INFO</a> by including client type information.

## -struct-fields

### -field ClientIpAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the assigned IP address of the DHCP client.

### -field SubnetMask

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_MASK</a> value that contains the subnet mask value assigned to the DHCP client.

### -field ClientHardwareAddress

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_CLIENT_UID</a> structure containing the MAC address of the client's network interface device.

### -field ClientName

Unicode string that specifies the network name of the DHCP client. This member is optional.

### -field ClientComment

Unicode string that contains a comment associated with the DHCP client. This member is optional.

### -field ClientLeaseExpires

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a> structure that contains the date and time the DHCP client lease will expire, in UTC time.

### -field OwnerHost

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a> structure that contains information on the DHCP server that assigned the IP address to the  client.

### -field bClientType

Specifies the types of dynamic IP address service used by the client.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_UNSPECIFIED"></a><a id="client_type_unspecified"></a><dl>
<dt><b>CLIENT_TYPE_UNSPECIFIED</b></dt>
</dl>
</td>
<td width="60%">
The client's dynamic IP address protocol is unknown.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_DHCP"></a><a id="client_type_dhcp"></a><dl>
<dt><b>CLIENT_TYPE_DHCP</b></dt>
</dl>
</td>
<td width="60%">
The client uses DHCP for dynamic IP address service.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOOTP"></a><a id="client_type_bootp"></a><dl>
<dt><b>CLIENT_TYPE_BOOTP</b></dt>
</dl>
</td>
<td width="60%">
The client uses BOOTP for dynamic IP address service.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOTH"></a><a id="client_type_both"></a><dl>
<dt><b>CLIENT_TYPE_BOTH</b></dt>
</dl>
</td>
<td width="60%">
The client can use either DHCP or BOOTP for dynamic IP address service.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_NONE"></a><a id="client_type_none"></a><dl>
<dt><b>CLIENT_TYPE_NONE</b></dt>
</dl>
</td>
<td width="60%">
The client does not use a supported dynamic IP address service.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_array_v4">DHCP_CLIENT_INFO_ARRAY_V4</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_CLIENT_UID</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetclientinfov4">DhcpGetClientInfoV4</a>