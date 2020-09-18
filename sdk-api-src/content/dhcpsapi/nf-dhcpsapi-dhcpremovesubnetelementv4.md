---
UID: NF:dhcpsapi.DhcpRemoveSubnetElementV4
title: DhcpRemoveSubnetElementV4 function (dhcpsapi.h)
description: Removes an IPv4 subnet element from an IPv4 subnet defined on the DHCPv4 server. The function extends the functionality provided by DhcpRemoveSubnetElement by allowing the specification of a subnet that contains client type (DHCP or BOOTP) information.
helpviewer_keywords: ["DhcpRemoveSubnetElementV4","DhcpRemoveSubnetElementV4 function [DHCP]","dhcp.dhcpremovesubnetelementv4","dhcpsapi/DhcpRemoveSubnetElementV4"]
old-location: dhcp\dhcpremovesubnetelementv4.htm
tech.root: DHCP
ms.assetid: 30edda5e-17de-46ec-9a6a-eab26a6ed29a
ms.date: 12/05/2018
ms.keywords: DhcpRemoveSubnetElementV4, DhcpRemoveSubnetElementV4 function [DHCP], dhcp.dhcpremovesubnetelementv4, dhcpsapi/DhcpRemoveSubnetElementV4
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
 - DhcpRemoveSubnetElementV4
 - dhcpsapi/DhcpRemoveSubnetElementV4
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
 - DhcpRemoveSubnetElementV4
---

# DhcpRemoveSubnetElementV4 function


## -description

The <b>DhcpRemoveSubnetElementV4</b> function removes an IPv4 subnet element from an IPv4 subnet defined on the DHCPv4 server. The function extends the functionality provided by <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpremovesubnetelement">DhcpRemoveSubnetElement</a> by allowing the specification of a subnet that contains client type (DHCP or BOOTP) information.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the IP address of the subnet gateway and uniquely identifies it.

### -param RemoveElementInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v4">DHCP_SUBNET_ELEMENT_DATA_V4</a> structure that contains information used to find the element that will be removed from subnet specified in <i>SubnetAddress</i>.

### -param ForceFlag [in]

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_force_flag">DHCP_FORCE_FLAG</a> enumeration value that indicates whether or not the clients affected by the removal of the subnet element should also be deleted.

<div class="alert"><b>Note</b>  If the flag is set to <b>DhcpNoForce</b> and this subnet has served an IPv4 address to DHCPv4/BOOTP clients, the IPv4 range is not deleted; conversely, if the flag is set to <b>DhcpFullForce</b>, the IPv4 range is deleted along with the DHCPv4 client lease record on the DHCPv4 server.</div>
<div> </div>

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
The specified IPv4 subnet is not defined on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP client is a reserved client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_INVALID_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 address range either overlaps an existing IPv4 address range, or is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_ELEMENT_CANT_REMOVE</b></dt>
</dl>
</td>
<td width="60%">
At least one multicast IPv4 address has been leased out to a MADCAP client.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_force_flag">DHCP_FORCE_FLAG</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v4">DHCP_SUBNET_ELEMENT_DATA_V4</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpaddsubnetelementv4">DhcpAddSubnetElementV4</a>