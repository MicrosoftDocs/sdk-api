---
UID: NF:dhcpsapi.DhcpCreateClientInfo
title: DhcpCreateClientInfo function (dhcpsapi.h)
description: The DhcpCreateClientInfo function creates a client information record on the DHCP server.
helpviewer_keywords: ["DhcpCreateClientInfo","DhcpCreateClientInfo function [DHCP]","dhcp.dhcpcreateclientinfo","dhcpsapi/DhcpCreateClientInfo"]
old-location: dhcp\dhcpcreateclientinfo.htm
tech.root: DHCP
ms.assetid: 121718db-a7d8-42b7-b1a1-5c2dbe7d3d6b
ms.date: 12/05/2018
ms.keywords: DhcpCreateClientInfo, DhcpCreateClientInfo function [DHCP], dhcp.dhcpcreateclientinfo, dhcpsapi/DhcpCreateClientInfo
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
 - DhcpCreateClientInfo
 - dhcpsapi/DhcpCreateClientInfo
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
 - DhcpCreateClientInfo
---

# DhcpCreateClientInfo function


## -description

The <b>DhcpCreateClientInfo</b> function creates a client information record on the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ClientInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info">DHCP_CLIENT_INFO</a> structure that contains information about the DHCP client, including the assigned IP address, subnet mask, and host.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

This function requires host byte ordering for all <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> values in parameter structures.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info">DHCP_CLIENT_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpdeleteclientinfo">DhcpDeleteClientInfo</a>