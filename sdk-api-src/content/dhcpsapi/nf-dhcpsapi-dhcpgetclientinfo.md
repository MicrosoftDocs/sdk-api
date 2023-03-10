---
UID: NF:dhcpsapi.DhcpGetClientInfo
title: DhcpGetClientInfo function (dhcpsapi.h)
description: The DhcpGetClientInfo function returns information about a specific DHCP client.
helpviewer_keywords: ["DhcpGetClientInfo","DhcpGetClientInfo function [DHCP]","dhcp.dhcpgetclientinfo","dhcpsapi/DhcpGetClientInfo"]
old-location: dhcp\dhcpgetclientinfo.htm
tech.root: DHCP
ms.assetid: 67095868-7e02-4d82-b2f0-70c413fa8ed6
ms.date: 12/05/2018
ms.keywords: DhcpGetClientInfo, DhcpGetClientInfo function [DHCP], dhcp.dhcpgetclientinfo, dhcpsapi/DhcpGetClientInfo
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
 - DhcpGetClientInfo
 - dhcpsapi/DhcpGetClientInfo
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
 - DhcpGetClientInfo
---

# DhcpGetClientInfo function


## -description

The <b>DhcpGetClientInfo</b> function returns information about  a specific DHCP client.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SearchInfo [in]

<a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_search_info">DHCP_SEARCH_INFO</a> structure that contains the parameters for the search.

### -param ClientInfo [out]

Pointer to a  <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info">DHCP_CLIENT_INFO</a> structure that contains information describing the DHCP client that most closely matches the provided search parameters. If no client is found, this parameter will be null.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

This function requires host byte ordering for all <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> values in parameter structures.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info">DHCP_CLIENT_INFO</a>



<a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_search_info">DHCP_SEARCH_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetclientinfo">DhcpSetClientInfo</a>