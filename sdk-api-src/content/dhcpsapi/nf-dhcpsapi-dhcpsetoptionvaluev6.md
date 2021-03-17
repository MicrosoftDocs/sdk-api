---
UID: NF:dhcpsapi.DhcpSetOptionValueV6
title: DhcpSetOptionValueV6 function (dhcpsapi.h)
description: The DhcpSetOptionValueV6 function sets information for a specific option value on the DHCP server.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpSetOptionValueV6","DhcpSetOptionValueV6 function [DHCP]","dhcp.dhcpsetoptionvaluev6","dhcpsapi/DhcpSetOptionValueV6"]
old-location: dhcp\dhcpsetoptionvaluev6.htm
tech.root: DHCP
ms.assetid: 1adfcefa-4f63-4a4c-9a78-3c91d32a9e13
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpSetOptionValueV6, DhcpSetOptionValueV6 function [DHCP], dhcp.dhcpsetoptionvaluev6, dhcpsapi/DhcpSetOptionValueV6
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
 - DhcpSetOptionValueV6
 - dhcpsapi/DhcpSetOptionValueV6
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
 - DhcpSetOptionValueV6
---

# DhcpSetOptionValueV6 function


## -description

The <b>DhcpSetOptionValueV6</b> function sets information for a specific option value on the DHCP server.

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
This flag should be set if the option is provided by a vendor.

</td>
</tr>
</table>

### -param OptionId [in]

DHCP_OPTION_ID value that contains the unique option ID number (also called an "option code") of the option being set. Many of these option ID numbers are defined; a complete list of standard DHCP and BOOTP option codes can be found at <a href="http://www.ietf.org/rfc/rfc2132.txt">http://www.ietf.org/rfc/rfc2132.txt</a>.

### -param ClassName [in]

Unicode string that specifies the DHCP  class  of the option. This parameter is optional.

### -param VendorName [in]

Unicode string that specifies the vendor of the option. This parameter is optional, and should be <b>NULL</b> when <i>Flags</i> is not set to DHCP_FLAGS_OPTION_IS_VENDOR.

### -param ScopeInfo [in]

Pointer to a DHCP_OPTION_SCOPE_INFO6 structure that contains information describing the DHCP scope this option value will be set on.

### -param OptionValue [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data">DHCP_OPTION_DATA</a> structure that contains the data value corresponding to the DHCP option code specified by <i>OptionID</i>.

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
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option is not present on the DHCP server.

</td>
</tr>
</table>