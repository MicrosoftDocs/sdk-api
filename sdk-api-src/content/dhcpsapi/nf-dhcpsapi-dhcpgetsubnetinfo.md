---
UID: NF:dhcpsapi.DhcpGetSubnetInfo
title: DhcpGetSubnetInfo function (dhcpsapi.h)
description: The DhcpGetSubnetInfo function returns information on a specific subnet.
helpviewer_keywords: ["DhcpGetSubnetInfo","DhcpGetSubnetInfo function [DHCP]","dhcp.dhcpgetsubnetinfo","dhcpsapi/DhcpGetSubnetInfo"]
old-location: dhcp\dhcpgetsubnetinfo.htm
tech.root: DHCP
ms.assetid: 0e511993-a9c3-445b-bafc-3d66182ee32d
ms.date: 12/05/2018
ms.keywords: DhcpGetSubnetInfo, DhcpGetSubnetInfo function [DHCP], dhcp.dhcpgetsubnetinfo, dhcpsapi/DhcpGetSubnetInfo
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - DhcpGetSubnetInfo
 - dhcpsapi/DhcpGetSubnetInfo
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
 - DhcpGetSubnetInfo
---

# DhcpGetSubnetInfo function


## -description

The <b>DhcpGetSubnetInfo</b> function returns information on a specific subnet.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the subnet ID.

### -param SubnetInfo [out]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info">DHCP_SUBNET_INFO</a> structure that contains the returned information for the subnet matching the ID specified by <i>SubnetAddress</i>.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

This function uses host byte ordering for all <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> values in the <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info">DHCP_SUBNET_INFO</a> structure passed back to the caller in the <i>SubnetInfo</i> parameter. However, this function uses network byte order for the <b>IpAddress</b> member of the <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_host_info">DHCP_HOST_INFO</a> structure within the <b>DHCP_SUBNET_INFO</b> structure.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info">DHCP_SUBNET_INFO</a>