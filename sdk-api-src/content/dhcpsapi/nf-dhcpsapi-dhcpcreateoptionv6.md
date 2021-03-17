---
UID: NF:dhcpsapi.DhcpCreateOptionV6
title: DhcpCreateOptionV6 function (dhcpsapi.h)
description: The DhcpCreateOptionV6 function creates a DHCP option.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpCreateOptionV6","DhcpCreateOptionV6 function [DHCP]","dhcp.dhcpcreateoptionv6","dhcpsapi/DhcpCreateOptionV6"]
old-location: dhcp\dhcpcreateoptionv6.htm
tech.root: DHCP
ms.assetid: c1a54d82-3fea-4f65-be46-d2a81d639429
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpCreateOptionV6, DhcpCreateOptionV6 function [DHCP], dhcp.dhcpcreateoptionv6, dhcpsapi/DhcpCreateOptionV6
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - DhcpCreateOptionV6
 - dhcpsapi/DhcpCreateOptionV6
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
 - DhcpCreateOptionV6
---

# DhcpCreateOptionV6 function


## -description

The <b>DhcpCreateOptionV6</b> function creates a DHCP option.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param Flags [in]

Specifies a bit flag that indicates whether or not the option is vendor-specific. If it is not, this parameter should be 0.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
</dl>
</td>
<td width="60%">
This flag must be set if the option is provided by a vendor.

</td>
</tr>
</table>

### -param OptionId [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that contains the unique option ID number (also called an "option code") of the new option. Many of these option ID numbers are defined; a complete list of standard DHCP and BOOTP option codes can be found at <a href="https://www.ietf.org/rfc/rfc3315.txt">http://www.ietf.org/rfc/rfc3315.txt</a>.

### -param ClassName [in, optional]

Unicode string that specifies the name of the DHCP class that will contain this option. This field is optional.

### -param VendorName [in, optional]

Unicode string that contains a vendor name string if the class specified in <i>ClassName</i> is a vendor-specific class.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DUPLICATE_TAG</b></dt>
</dl>
</td>
<td width="60%">
The specified scope already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The vendor name is invalid. Typically, this is because the vendor name is greater than 255 characters in length.

</td>
</tr>
</table>