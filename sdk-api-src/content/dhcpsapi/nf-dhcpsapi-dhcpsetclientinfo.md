---
UID: NF:dhcpsapi.DhcpSetClientInfo
title: DhcpSetClientInfo function (dhcpsapi.h)
description: The DhcpSetClientInfo function sets information on a client whose IP address lease is administrated by the DHCP server.
helpviewer_keywords: ["DhcpSetClientInfo","DhcpSetClientInfo function [DHCP]","dhcp.dhcpsetclientinfo","dhcpsapi/DhcpSetClientInfo"]
old-location: dhcp\dhcpsetclientinfo.htm
tech.root: DHCP
ms.assetid: 1eedddce-8b3e-419e-a065-163b22a0e9a8
ms.date: 12/05/2018
ms.keywords: DhcpSetClientInfo, DhcpSetClientInfo function [DHCP], dhcp.dhcpsetclientinfo, dhcpsapi/DhcpSetClientInfo
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
 - DhcpSetClientInfo
 - dhcpsapi/DhcpSetClientInfo
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
 - DhcpSetClientInfo
---

# DhcpSetClientInfo function


## -description

The <b>DhcpSetClientInfo</b> function sets information on a client whose IP address lease is administrated by the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ClientInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info">DHCP_CLIENT_INFO</a> structure that contains the information on a client in a subnet served by the DHCP server.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

This function requires host byte ordering for all <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> values in parameter structures.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info">DHCP_CLIENT_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetclientinfo">DhcpGetClientInfo</a>