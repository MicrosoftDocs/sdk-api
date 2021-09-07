---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_VQ
title: DHCP_CLIENT_INFO_VQ (dhcpsapi.h)
description: Defines information about the DHCPv4 client.
helpviewer_keywords: ["*LPDHCP_CLIENT_INFO_VQ","ADDRESS_STATE_ACTIVE","ADDRESS_STATE_DECLINED","ADDRESS_STATE_DOOM","ADDRESS_STATE_OFFERED","CLIENT_TYPE_BOOTP","CLIENT_TYPE_BOTH","CLIENT_TYPE_DHCP","CLIENT_TYPE_NONE","CLIENT_TYPE_RESERVATION_FLAG","CLIENT_TYPE_UNSPECIFIED","DHCP_CLIENT_INFO_VQ","DHCP_CLIENT_INFO_VQ structure [DHCP]","PDHCP_CLIENT_INFO_VQ","PDHCP_CLIENT_INFO_VQ structure pointer [DHCP]","dhcp.dhcp_client_info_vq","dhcpsapi/DHCP_CLIENT_INFO_VQ","dhcpsapi/PDHCP_CLIENT_INFO_VQ"]
old-location: dhcp\dhcp_client_info_vq.htm
tech.root: DHCP
ms.assetid: f7bd832d-b4a4-404c-8959-e9653b62d434
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLIENT_INFO_VQ, ADDRESS_STATE_ACTIVE, ADDRESS_STATE_DECLINED, ADDRESS_STATE_DOOM, ADDRESS_STATE_OFFERED, CLIENT_TYPE_BOOTP, CLIENT_TYPE_BOTH, CLIENT_TYPE_DHCP, CLIENT_TYPE_NONE, CLIENT_TYPE_RESERVATION_FLAG, CLIENT_TYPE_UNSPECIFIED, DHCP_CLIENT_INFO_VQ, DHCP_CLIENT_INFO_VQ structure [DHCP], PDHCP_CLIENT_INFO_VQ, PDHCP_CLIENT_INFO_VQ structure pointer [DHCP], dhcp.dhcp_client_info_vq, dhcpsapi/DHCP_CLIENT_INFO_VQ, dhcpsapi/PDHCP_CLIENT_INFO_VQ'
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
req.typenames: DHCP_CLIENT_INFO_VQ, *LPDHCP_CLIENT_INFO_VQ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLIENT_INFO_VQ
 - dhcpsapi/_DHCP_CLIENT_INFO_VQ
 - LPDHCP_CLIENT_INFO_VQ
 - dhcpsapi/LPDHCP_CLIENT_INFO_VQ
 - DHCP_CLIENT_INFO_VQ
 - dhcpsapi/DHCP_CLIENT_INFO_VQ
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
 - DHCP_CLIENT_INFO_VQ
---

# DHCP_CLIENT_INFO_VQ structure


## -description

The <b>DHCP_CLIENT_INFO_VQ</b> structure defines information about the DHCPv4 client.

## -struct-fields

### -field ClientIpAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> type value that contains the DHCPv4 client's IPv4 address.

### -field SubnetMask

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP IP_MASK</a> type value that contains the DHCPv4 client's IPv4 subnet mask address.

### -field ClientHardwareAddress

GUID value that contains the hardware address (MAC address) of the DHCPv4 client.

### -field ClientName

Ppointer to a null-terminated Unicode string that represents the DHCPv4 client's machine name.

### -field ClientComment

Pointer to a null-terminated Unicode string that represents the description given to the DHCPv4 client.

### -field ClientLeaseExpires

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a> structure that contains the lease expiry time for the DHCPv4 client. This is UTC time represented in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> format.

### -field OwnerHost

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a> structure that contains information about the host machine (DHCPv4 server machine) that has provided a lease to the DHCPv4 client.

### -field bClientType

Possible types of the DHCPv4 client. The possible values are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_UNSPECIFIED"></a><a id="client_type_unspecified"></a><dl>
<dt><b>CLIENT_TYPE_UNSPECIFIED</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
A DHCPv4 client other than ones defined in this table.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_DHCP"></a><a id="client_type_dhcp"></a><dl>
<dt><b>CLIENT_TYPE_DHCP</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client supports the DHCP protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOOTP"></a><a id="client_type_bootp"></a><dl>
<dt><b>CLIENT_TYPE_BOOTP</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client supports the BOOTP protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_BOTH"></a><a id="client_type_both"></a><dl>
<dt><b>CLIENT_TYPE_BOTH</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client understands both the DHCPv4 and the BOOTP protocols.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_RESERVATION_FLAG"></a><a id="client_type_reservation_flag"></a><dl>
<dt><b>CLIENT_TYPE_RESERVATION_FLAG</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
There is an IPv4 reservation created for the DHCPv4 client.

</td>
</tr>
<tr>
<td width="40%"><a id="CLIENT_TYPE_NONE"></a><a id="client_type_none"></a><dl>
<dt><b>CLIENT_TYPE_NONE</b></dt>
<dt>0x64</dt>
</dl>
</td>
<td width="60%">
Backward compatibility for manual addressing.

</td>
</tr>
</table>

### -field AddressState

Possible states of the IPv4 address given to the DHCPv4 client. The following table represents the different values and their meanings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_OFFERED"></a><a id="address_state_offered"></a><dl>
<dt><b>ADDRESS_STATE_OFFERED</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client has been offered this IPv4 address.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_ACTIVE"></a><a id="address_state_active"></a><dl>
<dt><b>ADDRESS_STATE_ACTIVE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The IPv4 address is active and has an active DHCPv4 client lease record.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_DECLINED"></a><a id="address_state_declined"></a><dl>
<dt><b>ADDRESS_STATE_DECLINED</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The IPv4 address request was declined by the DHCPv4 client; hence, it is a bad IPv4 address.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_DOOM"></a><a id="address_state_doom"></a><dl>
<dt><b>ADDRESS_STATE_DOOM</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
The IPv4 address is in DOOMED state and is due to be deleted.

</td>
</tr>
</table>

### -field Status

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-quarantinestatus">QuarantineStatus</a> enumeration that specifies possible health status values for the DHCPv4 client, as validated at the NAP server.

### -field ProbationEnds

This is of type <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a>, containing the end time of the probation if the DHCPv4 client is on probation. For this time period, the DHCPv4 client has full access to the network.

### -field QuarantineCapable

If <b>TRUE</b>, the DHCPv4 client is quarantine-enabled; if <b>FALSE</b>, it is not.

## -remarks

<b>DHCP_CLIENT_INFO_VQ</b> augments the DHCP_CLIENT_INFO_V5  structure by including information relating to the NAP settings of the DHCPv4 client.

## -see-also

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP Server Management Type Definitions</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a>