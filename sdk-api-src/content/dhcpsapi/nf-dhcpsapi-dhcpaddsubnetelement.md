---
UID: NF:dhcpsapi.DhcpAddSubnetElement
title: DhcpAddSubnetElement function
author: windows-sdk-content
description: Adds an element describing a feature or aspect of the subnet to the subnet entry in the DHCP database.
old-location: dhcp\dhcpaddsubnetelement.htm
tech.root: DHCP
ms.assetid: 4f93d4e8-f41e-4df8-98cc-70a11be75eab
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpAddSubnetElement, DhcpAddSubnetElement function [DHCP], dhcp.dhcpaddsubnetelement, dhcpsapi/DhcpAddSubnetElement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpAddSubnetElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DhcpAddSubnetElement
: 
---

# DhcpAddSubnetElement function


## -description


The <b>DhcpAddSubnetElement</b> function adds an element describing a feature or aspect of the subnet to the subnet entry in the DHCP database.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that contains the IPv4 address of the subnet DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that contains the IPv4 address of the subnet.


### -param AddElementInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/d6c32be0-a080-42c1-b9bf-3f5da2c4dbe0">DHCP_SUBNET_ELEMENT_DATA</a> structure that contains information about the subnet element corresponding to the IPv4 subnet specified in <i>SubnetAddress</i>.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_INVALID_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 address range either overlaps an existing range or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_IPRANGE_CONV_ILLEGAL</b></dt>
</dl>
</td>
<td width="60%">
Conversion of a scope to a DHCPv4-only scope or to a BOOTP-only scope is not allowed when DHCPv4 and BOOTP clients are present in the scope to convert. Manually delete either the DHCPv4 or the BOOTP clients from the scope, as appropriate for the type of scope being created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_IPRANGE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 address range already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_MSCOPE_RANGE_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The multicast scope range must allow for at least 256 IPv4 addresses.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_NOT_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCPv4 client is not an IPv4 reserverdclient.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_RESERVEDIP_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 address or hardware address is in use by another DHCPv4 client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The specified address is not available.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/97ffcafd-a74e-49ed-9e68-043b62a9017a">DhcpAddSubnetElementV4</a>



<a href="https://msdn.microsoft.com/200fc8da-d05c-4502-9cfc-d1092c5d0417">DhcpAddSubnetElementV5</a>
 

 

