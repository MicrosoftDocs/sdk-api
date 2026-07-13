---
UID: NF:dhcpsapi.DhcpEnumSubnetClientsV4
title: DhcpEnumSubnetClientsV4 function (dhcpsapi.h)
description: Returns an enumerated list of client lease records with served IP addresses in the specified subnet.
helpviewer_keywords: ["DhcpEnumSubnetClientsV4","DhcpEnumSubnetClientsV4 function [DHCP]","dhcp.dhcpenumsubnetclientsv4","dhcpsapi/DhcpEnumSubnetClientsV4"]
old-location: dhcp\dhcpenumsubnetclientsv4.htm
tech.root: DHCP
ms.assetid: 3451dc35-4cd1-4430-a19f-f0aa0533ea4b
ms.date: 12/05/2018
ms.keywords: DhcpEnumSubnetClientsV4, DhcpEnumSubnetClientsV4 function [DHCP], dhcp.dhcpenumsubnetclientsv4, dhcpsapi/DhcpEnumSubnetClientsV4
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
 - DhcpEnumSubnetClientsV4
 - dhcpsapi/DhcpEnumSubnetClientsV4
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
 - DhcpEnumSubnetClientsV4
---

# DhcpEnumSubnetClientsV4 function


## -description

The <b>DhcpEnumSubnetClientsV4</b> function  returns an enumerated list of client lease records with served IP addresses in the specified subnet. This function extends the functionality provided in <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnetclients">DhcpEnumSubnetClients</a> by returning a list  of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v4">DHCP_CLIENT_INFO_V4</a> structures that contain the specific client type (DHCP and/or BOOTP).

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value containing the IP address of the subnet gateway.

### -param ResumeHandle [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. This parameter contains the last IPv4 address retrieved from the DHCPv4 client.

The presence of additional enumerable data is indicated when this function returns ERROR_MORE_DATA. If no additional enumerable data is available on the DHCPv4 server, ERROR_NO_MORE_ITEMS is returned.

### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of subnet client elements to return. If the number of remaining unenumerated elements (in bytes) is less than this value, then that amount will be returned. The minimum value is 1024 bytes, and the maximum value is 65536 bytes.

To retrieve all the subnet client elements for the default user and vendor class at the specified level, set this parameter to 0xFFFFFFFF.

### -param ClientInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_array_v4">DHCP_CLIENT_INFO_ARRAY_V4</a> structure that contains the DHCPv4 client lease record array. If no clients are available, this field will be null.

### -param ClientsRead [out]

Pointer to a DWORD value that specifies the number of client lease records returned in <i>ClientInfo</i>.

### -param ClientsTotal [out]

Pointer to a DWORD value that specifies the total number of client lease records remaining on the DHCPv4 server. For example, if there are 100 DHCPv4 lease records for an IPv4 subnet, and if 10 DHCPv4 lease records are enumerated per call, then this parameter would return a value of 90 after the first call.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
There are more elements available to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more elements left to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet does not exist on the DHCP server.

</td>
</tr>
</table>

## -remarks

The caller of this function must free the memory for <i>ClientInfo</i> after the call completes.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_array_v4">DHCP_CLIENT_INFO_ARRAY_V4</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnetclients">DhcpEnumSubnetClients</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnetclientsv5">DhcpEnumSubnetClientsV5</a>