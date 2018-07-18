---
UID: NS:dhcpsapi._DHCPV6_BIND_ELEMENT
title: "_DHCPV6_BIND_ELEMENT"
author: windows-sdk-content
description: Defines an IPv6 interface binding for the DHCP server over which it receives DHCPv6 packets.
old-location: dhcp\dhcpv6_bind_element.htm
old-project: dhcp
ms.assetid: 7c5b1d5d-7c91-46a8-aaa0-1d957430461d
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*LPDHCPV6_BIND_ELEMENT, DHCPV6_BIND_ELEMENT, DHCPV6_BIND_ELEMENT structure [DHCP], DHCP_ENDPOINT_FLAG_CANT_MODIFY, PDHCPV6_BIND_ELEMENT, PDHCPV6_BIND_ELEMENT structure pointer [DHCP], _DHCPV6_BIND_ELEMENT, dhcp.dhcpv6_bind_element, dhcpsapi/DHCPV6_BIND_ELEMENT, dhcpsapi/PDHCPV6_BIND_ELEMENT"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DHCPV6_BIND_ELEMENT, *LPDHCPV6_BIND_ELEMENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCPV6_BIND_ELEMENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

