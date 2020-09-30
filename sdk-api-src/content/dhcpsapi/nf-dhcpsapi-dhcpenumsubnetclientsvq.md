---
UID: NF:dhcpsapi.DhcpEnumSubnetClientsVQ
title: DhcpEnumSubnetClientsVQ function (dhcpsapi.h)
description: Retrieves all DHCP clients serviced from the specified IPv4 subnet.
helpviewer_keywords: ["DhcpEnumSubnetClientsVQ","DhcpEnumSubnetClientsVQ function [DHCP]","dhcp.dhcpenumsubnetclientsvq","dhcpsapi/DhcpEnumSubnetClientsVQ"]
old-location: dhcp\dhcpenumsubnetclientsvq.htm
tech.root: DHCP
ms.assetid: 4e5cd074-1e1f-43cb-9c8b-e1cca0b8f2a8
ms.date: 12/05/2018
ms.keywords: DhcpEnumSubnetClientsVQ, DhcpEnumSubnetClientsVQ function [DHCP], dhcp.dhcpenumsubnetclientsvq, dhcpsapi/DhcpEnumSubnetClientsVQ
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
 - DhcpEnumSubnetClientsVQ
 - dhcpsapi/DhcpEnumSubnetClientsVQ
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
 - DhcpEnumSubnetClientsVQ
---

# DhcpEnumSubnetClientsVQ function


## -description

The <b>DhcpEnumSubnetClientsVQ</b> function retrieves all DHCP clients serviced from the specified IPv4 subnet.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the IPv4 subnet for which the DHCP clients are returned. If this parameter is set to 0, the DHCP clients for all known IPv4 subnets are returned.

### -param ResumeHandle [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation on the DHCP server. Initially, this value must be set to 0. A successful call will return a handle value in this parameter, which can be passed to subsequent enumeration requests. The returned handle value is the last IPv4 address retrieved in the enumeration operation.

### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes to return in the enumeration operation. the minimum value is 1024 bytes, and the maximum value is 65536 bytes.

### -param ClientInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_array_vq">DHCP_CLIENT_INFO_ARRAY_VQ</a> structure that contains the DHCP client lease record set returned by the enumeration operation.

### -param ClientsRead [out]

Pointer to a value that specifies the number of DHCP client records returned in <i>ClientInfo</i>.

### -param ClientsTotal [out]

Pointer to a value that specifies the number of DHCP client record remaining and as-yet unreturned.  For example, if there are 100 DHCP client records for a given IPv4 subnet, and if 10 client records are enumerated per call, then after the first call this value would return 90.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
There are still unenumerated client lease records on the DHCP server for the provided IPv4 subnet. Please call this function again with the returned resume handle to obtain more of them.

</td>
</tr>
</table>

## -remarks

If <i>SubnetAddress</i> is set to zero (0), then all of the DHCP clients from all known IPv4 subnets.

The caller of this function must free the data pointed to by <i>ClientInfo</i>.