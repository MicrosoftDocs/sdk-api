---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

