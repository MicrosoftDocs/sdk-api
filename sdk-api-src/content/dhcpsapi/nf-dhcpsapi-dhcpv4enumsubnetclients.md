---
UID: NF:dhcpsapi.DhcpV4EnumSubnetClients
title: DhcpV4EnumSubnetClients function (dhcpsapi.h)
description: Enumerates all DHCP client records serviced from the specified IPv4 subnet.
helpviewer_keywords: ["DhcpV4EnumSubnetClients","DhcpV4EnumSubnetClients function [DHCP]","dhcp.dhcpv4enumsubnetclients","dhcpsapi/DhcpV4EnumSubnetClients"]
old-location: dhcp\dhcpv4enumsubnetclients.htm
tech.root: DHCP
ms.assetid: f6c6113b-fabd-4094-a160-8da7a139bdc4
ms.date: 12/05/2018
ms.keywords: DhcpV4EnumSubnetClients, DhcpV4EnumSubnetClients function [DHCP], dhcp.dhcpv4enumsubnetclients, dhcpsapi/DhcpV4EnumSubnetClients
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - DhcpV4EnumSubnetClients
 - dhcpsapi/DhcpV4EnumSubnetClients
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
 - DhcpV4EnumSubnetClients
---

# DhcpV4EnumSubnetClients function


## -description

The <b>DhcpV4EnumSubnetClients</b> function enumerates all DHCP client records serviced from the specified IPv4 subnet.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the IPv4 subnet address of the DHCP client records to enumerate. If set to 0, the DHCP client records for all known IPv4 subnets are returned.

### -param ResumeHandle [in, out]

Pointer to a  <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> structure that identifies this enumeration for use in subsequent calls to this function. Initially, this value should be zero on input. If successful, the returned value should be used for subsequent enumeration requests. The returned handle value is the last IPv4 address retrieved in the enumeration operation.

### -param PreferredMaximum [in]

The maximum number of bytes of client records to return in <i>ClientInfo</i>. The minimum value is 1024 bytes, and the maximum value is 65536 bytes.

### -param ClientInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_pb_array">DHCP_CLIENT_INFO_PB_ARRAY</a> structure that contains the DHCP client lease records set available for the specified subnet.

### -param ClientsRead [out]

Pointer to a <b>DWORD</b> that specifies the number of DHCP client records returned in <i>ClientInfo.</i>

### -param ClientsTotal [out]

Pointer to a <b>DWORD</b>  that specifies the number of client records on the DHCP server that have not yet been enumerated.

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client who is not a member of the <i>DHCP Users</i> or <i>DHCP Administrators</i> security groups.

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
There are still non-enumerated client lease records on the DHCP server for the provided IPv4 subnet. Call this function again with the returned resume handle to obtain more records.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no client lease records on the DHCP server.

</td>
</tr>
</table>

## -remarks

<i>ClientInfo</i> should be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.