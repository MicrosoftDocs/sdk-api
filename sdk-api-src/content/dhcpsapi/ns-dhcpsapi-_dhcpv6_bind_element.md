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

# _DHCPV6_BIND_ELEMENT structure


## -description


The <b>DHCPV6_BIND_ELEMENT</b> structure defines an IPv6 interface binding for the DHCP server over which it receives DHCPv6 packets.


## -struct-fields




### -field Flags

A set of bit flags indicating properties of the interface binding.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_ENDPOINT_FLAG_CANT_MODIFY_"></a><a id="dhcp_endpoint_flag_cant_modify_"></a><dl>
<dt><b>DHCP_ENDPOINT_FLAG_CANT_MODIFY
</b></dt>
</dl>
</td>
<td width="60%">
The endpoints cannot be modified.


</td>
</tr>
</table>
 


### -field fBoundToDHCPServer

If <b>TRUE</b>, the interface is bound to the DHCPv6 server; if <b>FALSE</b>, it is not.


### -field AdapterPrimaryAddress


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that contains the IPv6 address assigned to the interface over which the DHCP server is receiving DHCPv6 packets.


### -field AdapterSubnetAddress


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that contains the IPv6 prefix ID of the subnet from which this interface is receiving DHCPv6 packets.


### -field IfDescription

Pointer to a null-terminated Unicode string that specifies the name assigned to this interface.


### -field IpV6IfIndex

Integer that specifies the IPv6 interface index of the current interface.


### -field IfIdSize

Integer that specifies the size of the interface GUID stored in <b>IfId</b>. 


### -field IfId

 Pointer to a BYTE blob that contains the GUID value assigned to this interface.


### -field IfId.size_is

 


### -field IfId.size_is.IfIdSize

 




## -see-also




<a href="https://msdn.microsoft.com/b78ebdf8-da24-418c-8fe8-aed3047dfdf3">DHCPV6_BIND_ELEMENT_ARRAY</a>



<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a>
 

 

