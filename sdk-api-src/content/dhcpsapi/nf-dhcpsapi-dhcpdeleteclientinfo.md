---
UID: NF:dhcpsapi.DhcpDeleteClientInfo
title: DhcpDeleteClientInfo function (dhcpsapi.h)
description: The DhcpDeleteClientInfo function deletes a client information record from the DHCP server.
helpviewer_keywords: ["DhcpDeleteClientInfo","DhcpDeleteClientInfo function [DHCP]","dhcp.dhcpdeleteclientinfo","dhcpsapi/DhcpDeleteClientInfo"]
old-location: dhcp\dhcpdeleteclientinfo.htm
tech.root: DHCP
ms.assetid: abbf4843-2a4f-4d09-9a21-33587ad0d3e8
ms.date: 12/05/2018
ms.keywords: DhcpDeleteClientInfo, DhcpDeleteClientInfo function [DHCP], dhcp.dhcpdeleteclientinfo, dhcpsapi/DhcpDeleteClientInfo
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
 - DhcpDeleteClientInfo
 - dhcpsapi/DhcpDeleteClientInfo
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
 - DhcpDeleteClientInfo
---

# DhcpDeleteClientInfo function


## -description

The <b>DhcpDeleteClientInfo</b> function deletes a client information record from the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ClientInfo [in]

<a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_search_info">DHCP_SEARCH_INFO</a> union structure that contains one of the following items used to search the DHCP client record database: the client IP address, the client MAC address, or the client network name. All records matching the value will be deleted; for example, if a client IP address of 192.1.1.10 is supplied, all records with this address in the <b>ClientIpAddress</b> field will be deleted.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -remarks

This function requires host byte ordering for all <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> values in parameter structures.

## -see-also

<a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_search_info">DHCP_SEARCH_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreateclientinfo">DhcpCreateClientInfo</a>