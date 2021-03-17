---
UID: NF:dhcpsapi.DhcpAddSubnetElementV4
title: DhcpAddSubnetElementV4 function (dhcpsapi.h)
description: Adds an element describing a feature or aspect of the subnet to the subnet entry in the DHCP database. This function extends DhcpAddSubnetElement by incorporating subnet elements that consider client type.
helpviewer_keywords: ["DhcpAddSubnetElementV4","DhcpAddSubnetElementV4 function [DHCP]","dhcp.dhcpaddsubnetelementv4","dhcpsapi/DhcpAddSubnetElementV4"]
old-location: dhcp\dhcpaddsubnetelementv4.htm
tech.root: DHCP
ms.assetid: 97ffcafd-a74e-49ed-9e68-043b62a9017a
ms.date: 12/05/2018
ms.keywords: DhcpAddSubnetElementV4, DhcpAddSubnetElementV4 function [DHCP], dhcp.dhcpaddsubnetelementv4, dhcpsapi/DhcpAddSubnetElementV4
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpAddSubnetElementV4
 - dhcpsapi/DhcpAddSubnetElementV4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpAddSubnetElementV4
---

# DhcpAddSubnetElementV4 function


## -description

The <b>DhcpAddSubnetElementV4</b> function adds an element describing a feature or aspect of the subnet to the subnet entry in the DHCP database. This function extends <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpaddsubnetelement">DhcpAddSubnetElement</a> by incorporating subnet elements that consider client type.
<div class="alert"><b>Note</b>  This function is not available in Windows previous to Windows NT 4.0 Service Pack 1.</div><div> </div>

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that contains the IP address of the subnet DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the IP address of the subnet.

### -param AddElementInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v4">DHCP_SUBNET_ELEMENT_DATA_V4</a> structure that contains the element data to add to the subnet. The V4 structure adds support for differentiation between DHCP and BOOTP clients.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

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
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition does not exist in the DHCP server database.

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

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v4">DHCP_SUBNET_ELEMENT_DATA_V4</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpaddsubnetelement">DhcpAddSubnetElement</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpaddsubnetelementv5">DhcpAddSubnetElementV5</a>