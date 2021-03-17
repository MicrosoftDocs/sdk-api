---
UID: NF:dhcpsapi.DhcpSetSubnetInfo
title: DhcpSetSubnetInfo function (dhcpsapi.h)
description: The DhcpSetSubnetInfo function sets information about a subnet defined on the DHCP server.
helpviewer_keywords: ["DhcpSetSubnetInfo","DhcpSetSubnetInfo function [DHCP]","dhcp.dhcpsetsubnetinfo","dhcpsapi/DhcpSetSubnetInfo"]
old-location: dhcp\dhcpsetsubnetinfo.htm
tech.root: DHCP
ms.assetid: a7978da5-945f-4893-83a8-5986c55703a5
ms.date: 12/05/2018
ms.keywords: DhcpSetSubnetInfo, DhcpSetSubnetInfo function [DHCP], dhcp.dhcpsetsubnetinfo, dhcpsapi/DhcpSetSubnetInfo
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
 - DhcpSetSubnetInfo
 - dhcpsapi/DhcpSetSubnetInfo
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
 - DhcpSetSubnetInfo
---

# DhcpSetSubnetInfo function


## -description

The <b>DhcpSetSubnetInfo</b> function sets information about a subnet defined on the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the IP address of the subnet gateway, as well as uniquely identifies the subnet.

### -param SubnetInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info">DHCP_SUBNET_INFO</a> structure that contains the information about the subnet.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info">DHCP_SUBNET_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetsubnetinfo">DhcpGetSubnetInfo</a>