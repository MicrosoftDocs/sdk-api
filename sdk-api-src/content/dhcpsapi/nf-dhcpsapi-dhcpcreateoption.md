---
UID: NF:dhcpsapi.DhcpCreateOption
title: DhcpCreateOption function (dhcpsapi.h)
description: Creates an option definition for the default user and vendor class at the default option level.
helpviewer_keywords: ["DhcpCreateOption","DhcpCreateOption function [DHCP]","dhcp.dhcpcreateoption","dhcpsapi/DhcpCreateOption"]
old-location: dhcp\dhcpcreateoption.htm
tech.root: DHCP
ms.assetid: 2a77467e-12e8-4a8e-a6ab-e3783a7492da
ms.date: 12/05/2018
ms.keywords: DhcpCreateOption, DhcpCreateOption function [DHCP], dhcp.dhcpcreateoption, dhcpsapi/DhcpCreateOption
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
 - DhcpCreateOption
 - dhcpsapi/DhcpCreateOption
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
 - DhcpCreateOption
---

# DhcpCreateOption function


## -description

The <b>DhcpCreateOption</b> function creates an option definition for the default user and vendor class at the default option level.

## -parameters

### -param ServerIpAddress [in]

Unicode string containing the IPv4 address of the DHCP server.

### -param OptionID [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that contains the unique option ID number (also called an "option code") of the new option. Many of these option ID numbers are defined; a complete list of standard DHCP and BOOTP option codes can be found in  <a href="https://www.ietf.org/rfc/rfc2132.txt">DHCP Options and BOOTP Vendor Extensions</a>.

### -param OptionInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option">DHCP_OPTION</a> structure that contains information describing the new   DHCP option, including the name, an optional comment, and any related data items.

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
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_OPTION_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition already exists in the DHCP server database.

</td>
</tr>
</table>

## -remarks

An option is a client configuration parameter assigned by a DHCP server to DHCP and BOOTP clients. For example, some commonly used options include IP addresses for gateways (subnet routers), WINS servers, and DNS servers. Typically, these options are enabled and configured for a particular scope, but default options can be created for all scopes served by a given DHCP server.

## -see-also

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreateoptionv5">DhcpCreateOptionV5</a>