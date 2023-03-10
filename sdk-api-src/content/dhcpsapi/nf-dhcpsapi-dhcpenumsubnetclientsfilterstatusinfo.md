---
UID: NF:dhcpsapi.DhcpEnumSubnetClientsFilterStatusInfo
title: DhcpEnumSubnetClientsFilterStatusInfo function (dhcpsapi.h)
description: Enumerates all of the DHCP clients serviced on the specified subnet, and includes link-layer filter status for each of them.
helpviewer_keywords: ["DhcpEnumSubnetClientsFilterStatusInfo","DhcpEnumSubnetClientsFilterStatusInfo function [DHCP]","dhcp.dhcpenumsubnetclientsfilterstatusinfo","dhcpsapi/DhcpEnumSubnetClientsFilterStatusInfo"]
old-location: dhcp\dhcpenumsubnetclientsfilterstatusinfo.htm
tech.root: DHCP
ms.assetid: a88455ca-ba64-46d0-af8f-be90c57d96f3
ms.date: 12/05/2018
ms.keywords: DhcpEnumSubnetClientsFilterStatusInfo, DhcpEnumSubnetClientsFilterStatusInfo function [DHCP], dhcp.dhcpenumsubnetclientsfilterstatusinfo, dhcpsapi/DhcpEnumSubnetClientsFilterStatusInfo
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
 - DhcpEnumSubnetClientsFilterStatusInfo
 - dhcpsapi/DhcpEnumSubnetClientsFilterStatusInfo
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
 - DhcpEnumSubnetClientsFilterStatusInfo
---

# DhcpEnumSubnetClientsFilterStatusInfo function


## -description

The <b>DhcpEnumSubnetClientsFilterStatusInfo</b> function enumerates all of the DHCP clients serviced on the specified subnet, and includes link-layer filter status for each of them.

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

Pointer to a <a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_client_filter_status_info_array">DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY</a> structure that contains all of the DHCP clients serviced on the specified subnet, as well as any associated link-layer filter status information for each of them.

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

## -see-also

<a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_client_filter_status_info_array">DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY</a>