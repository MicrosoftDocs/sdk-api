---
UID: NF:dhcpsapi.DhcpCreateSubnetV6
title: DhcpCreateSubnetV6 function (dhcpsapi.h)
description: The DhcpCreateSubnetV6 function creates a new subnet on the DHCP server.
helpviewer_keywords: ["DhcpCreateSubnetV6","DhcpCreateSubnetV6 function [DHCP]","dhcp.dhcpcreatesubnetv6","dhcpsapi/DhcpCreateSubnetV6"]
old-location: dhcp\dhcpcreatesubnetv6.htm
tech.root: DHCP
ms.assetid: a27ac111-39bf-4695-989a-1c83e7704ff4
ms.date: 12/05/2018
ms.keywords: DhcpCreateSubnetV6, DhcpCreateSubnetV6 function [DHCP], dhcp.dhcpcreatesubnetv6, dhcpsapi/DhcpCreateSubnetV6
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - DhcpCreateSubnetV6
 - dhcpsapi/DhcpCreateSubnetV6
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
 - DhcpCreateSubnetV6
---

# DhcpCreateSubnetV6 function


## -description

The <b>DhcpCreateSubnetV6</b> function creates a new subnet on the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

DHCP_IPV6_ADDRESS value that contains the IP address of the subnet's gateway.

### -param SubnetInfo [in]

DHCP_SUBNET_INFO_V6 structure that contains specific settings for the subnet, including the subnet mask and IP address of the  subnet gateway.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DUPLICATE_TAG</b></dt>
</dl>
</td>
<td width="60%">
The specified scope already exists.

</td>
</tr>
</table>