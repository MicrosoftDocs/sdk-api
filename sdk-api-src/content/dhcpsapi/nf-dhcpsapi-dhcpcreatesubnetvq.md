---
UID: NF:dhcpsapi.DhcpCreateSubnetVQ
title: DhcpCreateSubnetVQ function (dhcpsapi.h)
description: The DhcpCreateSubnetVQ function creates a new IPv4 subnet and its associated NAP state information on the DHCP server.
helpviewer_keywords: ["DhcpCreateSubnetVQ","DhcpCreateSubnetVQ function [DHCP]","dhcp.dhcpcreatesubnetvq","dhcpsapi/DhcpCreateSubnetVQ"]
old-location: dhcp\dhcpcreatesubnetvq.htm
tech.root: DHCP
ms.assetid: 4ec8cff5-0652-4dd0-9393-7131e3be6ef8
ms.date: 12/05/2018
ms.keywords: DhcpCreateSubnetVQ, DhcpCreateSubnetVQ function [DHCP], dhcp.dhcpcreatesubnetvq, dhcpsapi/DhcpCreateSubnetVQ
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
 - DhcpCreateSubnetVQ
 - dhcpsapi/DhcpCreateSubnetVQ
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
 - DhcpCreateSubnetVQ
---

# DhcpCreateSubnetVQ function


## -description

The <b>DhcpCreateSubnetVQ</b> function creates a new IPv4 subnet and its associated NAP state information on the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

A <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the IPv4 address of the subnet's gateway.

### -param SubnetInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info_vq">DHCP_SUBNET_INFO_VQ</a> structure that contains specific settings for the subnet, including the subnet mask and IPv4 address of the  subnet gateway.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>. Commonly returned error codes include:

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
<dt><b>ERROR_DHCP_SUBNET_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The IPv4 scope parameters specified in the <i>SubnetInfo</i> parameter are incorrect. Either the IPv4 scope already exists, or its subnet address and mask are inconsistent with the subnet address and mask of an existing scope.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info_vq">DHCP_SUBNET_INFO_VQ</a>