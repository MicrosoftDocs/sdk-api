---
UID: NF:dhcpsapi.DhcpEnumSubnetClientsV5
title: DhcpEnumSubnetClientsV5 function (dhcpsapi.h)
description: Returns an enumerated list of clients with served IP addresses in the specified subnet.
helpviewer_keywords: ["DhcpEnumSubnetClientsV5","DhcpEnumSubnetClientsV5 function [DHCP]","dhcp.dhcpenumsubnetclientsv5","dhcpsapi/DhcpEnumSubnetClientsV5"]
old-location: dhcp\dhcpenumsubnetclientsv5.htm
tech.root: DHCP
ms.assetid: 34be1d6d-10d5-4025-abc6-29857417e081
ms.date: 12/05/2018
ms.keywords: DhcpEnumSubnetClientsV5, DhcpEnumSubnetClientsV5 function [DHCP], dhcp.dhcpenumsubnetclientsv5, dhcpsapi/DhcpEnumSubnetClientsV5
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
 - DhcpEnumSubnetClientsV5
 - dhcpsapi/DhcpEnumSubnetClientsV5
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
 - DhcpEnumSubnetClientsV5
---

# DhcpEnumSubnetClientsV5 function


## -description

The <b>DhcpEnumSubnetClientsV5</b> function returns an enumerated list of clients with served IP addresses in the specified subnet. This function extends the features  provided in the <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnetclients">DhcpEnumSubnetClients</a> function by returning a list  of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v5">DHCP_CLIENT_INFO_V5</a> structures that contain the specific client type (DHCP and/or BOOTP) and the IP address state.

## -parameters

### -param ServerIpAddress [in]

A UNICODE string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

A  value containing the IP address of the subnet gateway. If this parameter is set to 0, then the DHCP clients for all IPv4 subnets defined on the DHCP server are returned.

### -param ResumeHandle [in, out]

A pointer to a handle that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes worth of subnet client information structures  are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth.

### -param PreferredMaximum [in]

The preferred maximum number of bytes of subnet client information structures to return. If the number of remaining unenumerated options (in bytes) is less than this value, then that amount will be returned.

### -param ClientInfo [out]

A pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_array_v5">DHCP_CLIENT_INFO_ARRAY_V5</a> structure containing information on the clients served under this specific subnet. If no clients are available, this field will be null.

### -param ClientsRead [out]

A pointer to a value that specifies the number of clients returned in <i>ClientInfo</i>.

### -param ClientsTotal [out]

A pointer to a value that specifies the total number of clients for the specified subnet stored on the DHCP server.

## -returns

The <b>DhcpEnumSubnetClientsV5</b> function returns <b>ERROR_SUCCESS</b> upon success. 

On error, the function returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

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
The call was performed by a client who is not a member of the "DHCP Administrators" security group.

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
There are still un-enumerated client lease records on the DHCP server for the provided IPv4 subnet. Please call this function again with the returned resume handle to obtain more of them.

</td>
</tr>
</table>

## -remarks

The caller of this function must release the memory used by the <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_array_v5">DHCP_CLIENT_INFO_ARRAY_V5</a> structure returned in buffer pointed to by the <i>ClientInfo</i> parameter when the information is no longer needed.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_array_v5">DHCP_CLIENT_INFO_ARRAY_V5</a>



<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a>



<b>DHCP_RESUME_HANDLE</b>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnetclients">DhcpEnumSubnetClients</a>