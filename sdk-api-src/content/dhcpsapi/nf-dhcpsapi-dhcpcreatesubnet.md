---
UID: NF:dhcpsapi.DhcpCreateSubnet
title: DhcpCreateSubnet function (dhcpsapi.h)
description: The DhcpCreateSubnet function creates a new subnet on the DHCP server.
helpviewer_keywords: ["DhcpCreateSubnet","DhcpCreateSubnet function [DHCP]","dhcp.dhcpcreatesubnet","dhcpsapi/DhcpCreateSubnet"]
old-location: dhcp\dhcpcreatesubnet.htm
tech.root: DHCP
ms.assetid: acae01cf-cbd9-4461-a1cc-5fcb745b9c8f
ms.date: 12/05/2018
ms.keywords: DhcpCreateSubnet, DhcpCreateSubnet function [DHCP], dhcp.dhcpcreatesubnet, dhcpsapi/DhcpCreateSubnet
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
 - DhcpCreateSubnet
 - dhcpsapi/DhcpCreateSubnet
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
 - DhcpCreateSubnet
---

# DhcpCreateSubnet function


## -description

The <b>DhcpCreateSubnet</b> function creates a new subnet on the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the IP address of the subnet's gateway.

### -param SubnetInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info">DHCP_SUBNET_INFO</a> structure that contains specific settings for the subnet, including the subnet mask and IP address of the  subnet gateway.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_info">DHCP_SUBNET_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpdeletesubnet">DhcpDeleteSubnet</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnets">DhcpEnumSubnets</a>