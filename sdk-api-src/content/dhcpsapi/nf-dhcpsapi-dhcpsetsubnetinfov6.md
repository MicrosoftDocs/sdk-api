---
UID: NF:dhcpsapi.DhcpSetSubnetInfoV6
title: DhcpSetSubnetInfoV6 function (dhcpsapi.h)
description: Sets or updates the information for an IPv6 subnet defined on the DHCPv6 server.
helpviewer_keywords: ["DhcpSetSubnetInfoV6","DhcpSetSubnetInfoV6 function [DHCP]","dhcp.dhcpsetsubnetinfov6","dhcpsapi/DhcpSetSubnetInfoV6"]
old-location: dhcp\dhcpsetsubnetinfov6.htm
tech.root: DHCP
ms.assetid: 6913881d-a7d5-4465-aadc-5a4dab1a28da
ms.date: 12/05/2018
ms.keywords: DhcpSetSubnetInfoV6, DhcpSetSubnetInfoV6 function [DHCP], dhcp.dhcpsetsubnetinfov6, dhcpsapi/DhcpSetSubnetInfoV6
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
 - DhcpSetSubnetInfoV6
 - dhcpsapi/DhcpSetSubnetInfoV6
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
 - DhcpSetSubnetInfoV6
---

# DhcpSetSubnetInfoV6 function


## -description

The <b>DhcpSetSubnetInfoV6</b> function sets or updates the information for an IPv6 subnet defined on the DHCPv6 server.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structure that contains the IPv6 address of the subnet for which the information will be modified.

### -param SubnetInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info_v6">DHCP_SUBNET_INFO_V6</a> structure that contains the new or updated information for the IPv6 subnet identified by <i>SubnetAddress</i>.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client who is not a member of the "DHCP Administrators" security group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server's database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified subnet is not defined on the DHCP server.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info_v6">DHCP_SUBNET_INFO_V6</a>