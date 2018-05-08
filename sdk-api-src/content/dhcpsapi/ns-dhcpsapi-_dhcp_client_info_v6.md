---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_V6
title: "_DHCP_CLIENT_INFO_V6"
author: windows-driver-content
description: The DHCP_CLIENT_INFO_V6 structure contains information on DHCPv6 clients.
old-location: dhcp\dhcp_client_info_v6.htm
old-project: DHCP
ms.assetid: c676878d-2186-4aa2-b912-dc89272902c6
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: "*LPDHCP_CLIENT_INFO_V6, ADDRESS_TYPE_IANA, ADDRESS_TYPE_IATA, DHCP_CLIENT_INFO_V6, DHCP_CLIENT_INFO_V6 structure [DHCP], PDHCP_CLIENT_INFO_V6, PDHCP_CLIENT_INFO_V6 structure pointer [DHCP], _DHCP_CLIENT_INFO_V6, dhcp.dhcp_client_info_v6, dhcpsapi/DHCP_CLIENT_INFO_V6, dhcpsapi/PDHCP_CLIENT_INFO_V6"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DHCP_CLIENT_INFO_V6, *LPDHCP_CLIENT_INFO_V6
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_CLIENT_INFO_V6
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_CLIENT_INFO_V6 structure


## -description


The <b>DHCP_CLIENT_INFO_V6</b> structure contains information on DHCPv6 clients.


## -struct-fields




### -field ClientIpAddress

This is of type <a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> (section 2.2.1.2.28), containing the DHCPv6 client's IPv6 address.


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

This is of type <a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a> (section 2.2.1.2.11), containing the valid lifetime of the DHCPv6 IPv6 client lease.


### -field ClientPrefLeaseExpires

This is of type <a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a>, containing the preferred lifetime of the DHCPv6 client lease.


### -field OwnerHost

This of type <a href="https://msdn.microsoft.com/7473bbcd-d032-4f44-96e8-e08f050c08a3">DHCP_HOST_INFO_V6</a> (section 2.2.1.2.63), containing information about the host machine (DHCPv6 server machine) that has given this IPv6 lease to this DHCPv6 client.


## -see-also




<a href="https://msdn.microsoft.com/7473bbcd-d032-4f44-96e8-e08f050c08a3">DHCP_HOST_INFO_V6</a>



<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a>
 

 

