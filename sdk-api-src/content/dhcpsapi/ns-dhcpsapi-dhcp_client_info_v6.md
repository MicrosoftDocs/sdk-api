---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_V6
title: DHCP_CLIENT_INFO_V6 (dhcpsapi.h)
description: The DHCP_CLIENT_INFO_V6 structure contains information on DHCPv6 clients.
helpviewer_keywords: ["*LPDHCP_CLIENT_INFO_V6","ADDRESS_TYPE_IANA","ADDRESS_TYPE_IATA","DHCP_CLIENT_INFO_V6","DHCP_CLIENT_INFO_V6 structure [DHCP]","PDHCP_CLIENT_INFO_V6","PDHCP_CLIENT_INFO_V6 structure pointer [DHCP]","dhcp.dhcp_client_info_v6","dhcpsapi/DHCP_CLIENT_INFO_V6","dhcpsapi/PDHCP_CLIENT_INFO_V6"]
old-location: dhcp\dhcp_client_info_v6.htm
tech.root: DHCP
ms.assetid: c676878d-2186-4aa2-b912-dc89272902c6
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLIENT_INFO_V6, ADDRESS_TYPE_IANA, ADDRESS_TYPE_IATA, DHCP_CLIENT_INFO_V6, DHCP_CLIENT_INFO_V6 structure [DHCP], PDHCP_CLIENT_INFO_V6, PDHCP_CLIENT_INFO_V6 structure pointer [DHCP], dhcp.dhcp_client_info_v6, dhcpsapi/DHCP_CLIENT_INFO_V6, dhcpsapi/PDHCP_CLIENT_INFO_V6'
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
req.typenames: DHCP_CLIENT_INFO_V6, *LPDHCP_CLIENT_INFO_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLIENT_INFO_V6
 - dhcpsapi/_DHCP_CLIENT_INFO_V6
 - LPDHCP_CLIENT_INFO_V6
 - dhcpsapi/LPDHCP_CLIENT_INFO_V6
 - DHCP_CLIENT_INFO_V6
 - dhcpsapi/DHCP_CLIENT_INFO_V6
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
 - DHCP_CLIENT_INFO_V6
---

# DHCP_CLIENT_INFO_V6 structure


## -description

The <b>DHCP_CLIENT_INFO_V6</b> structure contains information on DHCPv6 clients.

## -struct-fields

### -field ClientIpAddress

This is of type <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> (section 2.2.1.2.28), containing the DHCPv6 client's IPv6 address.

### -field ClientDUID

This is of type DHCP_CLIENT_UID (section 2.2.1.2.5), containing the DHCPv6 client identifier.

### -field AddressType

This is of type <b>DWORD</b>, specifying the type of IPv6 address.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_TYPE_IANA"></a><a id="address_type_iana"></a><dl>
<dt><b>ADDRESS_TYPE_IANA</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Indicates an IANA address. [RFC3315]

</td>
</tr>
<tr>
<td width="40%"><a id="ADDRESS_TYPE_IATA"></a><a id="address_type_iata"></a><dl>
<dt><b>ADDRESS_TYPE_IATA</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Indicates an IATA address. [RFC3315]

</td>
</tr>
</table>

### -field IAID

This is of type <b>DWORD</b>, specifying the interface identifier of the DHCPv6 client interface.

### -field ClientName

A pointer to a null-terminated Unicode string containing the name of the DHCPv6 client.

### -field ClientComment

A pointer to a null-terminated Unicode string containing a comment relating to the DHCPv6 client.

### -field ClientValidLeaseExpires

This is of type <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a> (section 2.2.1.2.11), containing the valid lifetime of the DHCPv6 IPv6 client lease.

### -field ClientPrefLeaseExpires

This is of type <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a>, containing the preferred lifetime of the DHCPv6 client lease.

### -field OwnerHost

This of type <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info_v6">DHCP_HOST_INFO_V6</a> (section 2.2.1.2.63), containing information about the host machine (DHCPv6 server machine) that has given this IPv6 lease to this DHCPv6 client.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info_v6">DHCP_HOST_INFO_V6</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a>