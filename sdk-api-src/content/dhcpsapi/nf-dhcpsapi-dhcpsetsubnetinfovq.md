---
UID: NF:dhcpsapi.DhcpSetSubnetInfoVQ
title: DhcpSetSubnetInfoVQ function (dhcpsapi.h)
description: Sets information about a subnet defined on the DHCP server.
helpviewer_keywords: ["DhcpSetSubnetInfoVQ","DhcpSetSubnetInfoVQ function [DHCP]","dhcp.dhcpsetsubnetinfovq","dhcpsapi/DhcpSetSubnetInfoVQ"]
old-location: dhcp\dhcpsetsubnetinfovq.htm
tech.root: DHCP
ms.assetid: 1e584377-aded-4888-9641-8b9e5b8d2f98
ms.date: 12/05/2018
ms.keywords: DhcpSetSubnetInfoVQ, DhcpSetSubnetInfoVQ function [DHCP], dhcp.dhcpsetsubnetinfovq, dhcpsapi/DhcpSetSubnetInfoVQ
f1_keywords:
- dhcpsapi/DhcpSetSubnetInfoVQ
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dhcpsapi.dll
api_name:
- DhcpSetSubnetInfoVQ
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DhcpSetSubnetInfoVQ function


## -description


The <b>DhcpSetSubnetInfoVQ</b> function sets information about a subnet defined on the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the IP address of the subnet gateway, as well as uniquely identifies the subnet.


### -param SubnetInfo [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info_vq">DHCP_SUBNET_INFO_VQ</a> structure that contains the information about the subnet.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

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
The specified IPv4 subnet is not defined on the DHCP server.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info_vq">DHCP_SUBNET_INFO_VQ</a>
 

 

