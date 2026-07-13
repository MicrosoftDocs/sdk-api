---
UID: NS:dhcpsapi._DHCPV4_FAILOVER_CLIENT_INFO
title: DHCPV4_FAILOVER_CLIENT_INFO (dhcpsapi.h)
description: The DHCPV4_FAILOVER_CLIENT_INFO structure defines DHCP server scope statistics that are part of a failover relationship.
helpviewer_keywords: ["*LPDHCPV4_FAILOVER_CLIENT_INFO","ADDRESS_BIT_BOTH_REC","ADDRESS_BIT_CLEANUP","ADDRESS_BIT_DELETED","ADDRESS_BIT_DHCID_NO_CLIENTIDOPTION","ADDRESS_BIT_DHCID_WITH_CLIENTIDOPTION","ADDRESS_BIT_DHCID_WITH_DUID","ADDRESS_BIT_NO_DHCID","ADDRESS_BIT_UNREGISTERED","ADDRESS_STATE_ACTIVE","ADDRESS_STATE_DECLINED","ADDRESS_STATE_DOOM","ADDRESS_STATE_OFFERED","CLIENT_TYPE_BOOTP","CLIENT_TYPE_BOTH","CLIENT_TYPE_DHCP","CLIENT_TYPE_NONE","CLIENT_TYPE_RESERVATION_FLAG","CLIENT_TYPE_UNSPECIFIED","DHCPV4_FAILOVER_CLIENT_INFO","DHCPV4_FAILOVER_CLIENT_INFO structure [DHCP]","LPDHCPV4_FAILOVER_CLIENT_INFO","LPDHCPV4_FAILOVER_CLIENT_INFO structure pointer [DHCP]","dhcp.dhcpv4_failover_client_info","dhcpsapi/DHCPV4_FAILOVER_CLIENT_INFO","dhcpsapi/LPDHCPV4_FAILOVER_CLIENT_INFO"]
old-location: dhcp\dhcpv4_failover_client_info.htm
tech.root: DHCP
ms.assetid: 46e4fb62-5b8e-44f8-b3a0-92535ca690f0
ms.date: 12/05/2018
ms.keywords: '*LPDHCPV4_FAILOVER_CLIENT_INFO, ADDRESS_BIT_BOTH_REC, ADDRESS_BIT_CLEANUP, ADDRESS_BIT_DELETED, ADDRESS_BIT_DHCID_NO_CLIENTIDOPTION, ADDRESS_BIT_DHCID_WITH_CLIENTIDOPTION, ADDRESS_BIT_DHCID_WITH_DUID, ADDRESS_BIT_NO_DHCID, ADDRESS_BIT_UNREGISTERED, ADDRESS_STATE_ACTIVE, ADDRESS_STATE_DECLINED, ADDRESS_STATE_DOOM, ADDRESS_STATE_OFFERED, CLIENT_TYPE_BOOTP, CLIENT_TYPE_BOTH, CLIENT_TYPE_DHCP, CLIENT_TYPE_NONE, CLIENT_TYPE_RESERVATION_FLAG, CLIENT_TYPE_UNSPECIFIED, DHCPV4_FAILOVER_CLIENT_INFO, DHCPV4_FAILOVER_CLIENT_INFO structure [DHCP], LPDHCPV4_FAILOVER_CLIENT_INFO, LPDHCPV4_FAILOVER_CLIENT_INFO structure pointer [DHCP], dhcp.dhcpv4_failover_client_info, dhcpsapi/DHCPV4_FAILOVER_CLIENT_INFO, dhcpsapi/LPDHCPV4_FAILOVER_CLIENT_INFO'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: DHCPV4_FAILOVER_CLIENT_INFO, *LPDHCPV4_FAILOVER_CLIENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPV4_FAILOVER_CLIENT_INFO
 - dhcpsapi/_DHCPV4_FAILOVER_CLIENT_INFO
 - LPDHCPV4_FAILOVER_CLIENT_INFO
 - dhcpsapi/LPDHCPV4_FAILOVER_CLIENT_INFO
 - DHCPV4_FAILOVER_CLIENT_INFO
 - dhcpsapi/DHCPV4_FAILOVER_CLIENT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCPV4_FAILOVER_CLIENT_INFO
---

## -description

The <b>DHCPV4_FAILOVER_CLIENT_INFO</b> structure defines DHCP server scope statistics that are part of a failover relationship.

## -struct-fields

### -field ClientIpAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the DHCPv4 client IPv4 address.

### -field SubnetMask

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_MASK</a> structure that contains the DHCPv4 client IPv4 subnet mask.

### -field ClientHardwareAddress

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_CLIENT_UID</a> structure that contains the hardware address (MAC address) of the DHCPv4 client.

### -field ClientName

Pointer to a null-terminated Unicode string that represents the DHCPv4 client machine name.

### -field ClientComment

Pointer to a null-terminated Unicode string that represents the description of the DHCPv4 client.

### -field ClientLeaseExpires

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a> structure that contains the lease expiry time for the DHCPv4 client. This is UTC time represented in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> format.

### -field OwnerHost

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a> structure that contains information about the host machine (DHCPv4 server) that provided a lease to the DHCPv4 client.

### -field bClientType

Value that specifies the DHCPv4 client type. The possible values are below.

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
The DHCPv4 client is not defined in the  server database.

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
The DHCPv4 client supports both the DHCPv4 and the BOOTP protocols

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

Value that specifies various states of the IPv4 address. The LSB is bit 0 and the MSB is bit 7. The possible values are below.

BIT 0 and BIT 1 signify the DHCPv4 client IPv4 address state, as shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_OFFERED"></a><a id="address_state_offered"></a><dl>
<dt><b>ADDRESS_STATE_OFFERED</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
The DHCPv4 client is offered this IPv4 address.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_ACTIVE"></a><a id="address_state_active"></a><dl>
<dt><b>ADDRESS_STATE_ACTIVE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The IPv4 address is active and has an active DHCPv4 client lease record.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_DECLINED"></a><a id="address_state_declined"></a><dl>
<dt><b>ADDRESS_STATE_DECLINED</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The IPv4 address request is declined by the DHCPv4 client; hence, it is a bad IPv4 address.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_STATE_DOOM"></a><a id="address_state_doom"></a><dl>
<dt><b>ADDRESS_STATE_DOOM</b></dt>
<dt>0x3</dt>
</dl>
</td>
<td width="60%">
The IPv4 address is in <i>DOOMED</i> state and is due to be deleted.

</td>
</tr>
</table>
 

BIT 2 and BIT 3 signify information related to Name Protection for the leased IPv4 address, as shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_BIT_NO_DHCID"></a><a id="address_bit_no_dhcid"></a><dl>
<dt><b>ADDRESS_BIT_NO_DHCID</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
The address is leased to the DHCPv4 client without <i>DHCID</i> as defined in sections 3 and 3.5 of <a href="http://www.faqs.org/rfcs/rfc4701.html">RFC4701</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_BIT_DHCID_NO_CLIENTIDOPTION"></a><a id="address_bit_dhcid_no_clientidoption"></a><dl>
<dt><b>ADDRESS_BIT_DHCID_NO_CLIENTIDOPTION</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The address is leased to the DHCPv4 client with <i>DHCID</i> but without the client ID option as defined in sections 3 and 3.5 of <a href="http://www.faqs.org/rfcs/rfc4701.html">RFC4701</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_BIT_DHCID_WITH_CLIENTIDOPTION"></a><a id="address_bit_dhcid_with_clientidoption"></a><dl>
<dt><b>ADDRESS_BIT_DHCID_WITH_CLIENTIDOPTION</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The address is leased to the DHCPv4 client with <i>DHCID</i> and the client ID option as defined in sections 3 and 3.5 of <a href="http://www.faqs.org/rfcs/rfc4701.html">RFC4701</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_BIT_DHCID_WITH_DUID"></a><a id="address_bit_dhcid_with_duid"></a><dl>
<dt><b>ADDRESS_BIT_DHCID_WITH_DUID</b></dt>
<dt>0x3</dt>
</dl>
</td>
<td width="60%">
The address is leased to the DHCPv4 client with <i>DHCID</i> and the client DUID and as defined in sections 3 and 3.5 of <a href="http://www.faqs.org/rfcs/rfc4701.html">RFC4701</a>.

</td>
</tr>
</table>
 

BIT 4, BIT 5, BIT 6, and BIT 7 specify information related to DNS, as shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_BIT_CLEANUP"></a><a id="address_bit_cleanup"></a><dl>
<dt><b>ADDRESS_BIT_CLEANUP</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The DNS update for the DHCPv4 client lease record needs to be deleted from the DNS server when the lease is deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_BIT_BOTH_REC"></a><a id="address_bit_both_rec"></a><dl>
<dt><b>ADDRESS_BIT_BOTH_REC</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The DNS update needs to be sent for both <a href="/windows/win32/api/windns/nf-windns-dnsquery_a">DNS_A_DATA</a> and <a href="/windows/win32/api/windns/nf-windns-dnsquery_w">DNS_PTR_DATA</a> type resource records.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_BIT_UNREGISTERED"></a><a id="address_bit_unregistered"></a><dl>
<dt><b>ADDRESS_BIT_UNREGISTERED</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The DNS update is not complete for the lease record.

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_BIT_DELETED"></a><a id="address_bit_deleted"></a><dl>
<dt><b>ADDRESS_BIT_DELETED</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
The address lease is expired, but the DNS updates for the lease record have not been deleted from the DNS server.

</td>
</tr>
</table>

### -field Status

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-quarantinestatus">QuarantineStatus</a> enumeration that specifies possible health status values for the DHCPv4 client as validated at the NAP server.

### -field ProbationEnds

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a> structure that contains the probation end time if the DHCPv4 client is on probation. The DHCPv4 client has full access to the network for this time period. This is UTC time represented in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> format.

### -field QuarantineCapable

<b>TRUE</b>, if the DHCPv4 client is quarantine-enabled; Otherwise, it is <b>FALSE</b>.

### -field SentPotExpTime

Time, in seconds, of potential-expiration-time sent to the partner server.

### -field AckPotExpTime

Time, in seconds, of potential-expiration-time acknowledged by the partner server.

### -field RecvPotExpTime

Time, in seconds, of potential-expiration-time received from the partner server.

### -field StartTime

Time, in seconds, since the client lease first entered into its current state.

### -field CltLastTransTime

Time, in seconds, since the client-last-transaction-time.

### -field LastBndUpdTime

Time, in seconds, since the partner server last updated the DHCPv4 client lease.

### -field BndMsgStatus

Reserved. Do not use.

### -field PolicyName

Pointer to a null-terminated Unicode string that represents the DHCP server policy name that resulted in the IPv4 address assignment to the DHCPv4 client in the lease.

### -field Flags

Reserved. Do not use.

## -see-also

<a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcpv4_failover_client_info_array">DHCPV4_FAILOVER_CLIENT_INFO_ARRAY</a>