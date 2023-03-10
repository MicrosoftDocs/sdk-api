---
UID: NF:dhcpsapi.DhcpRemoveOptionValueV5
title: DhcpRemoveOptionValueV5 function (dhcpsapi.h)
description: The DhcpRemoveOptionValueV5 function removes an option value from a scope defined on the DHCP server.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpRemoveOptionValueV5","DhcpRemoveOptionValueV5 function [DHCP]","dhcp.dhcpremoveoptionvaluev5","dhcpsapi/DhcpRemoveOptionValueV5"]
old-location: dhcp\dhcpremoveoptionvaluev5.htm
tech.root: DHCP
ms.assetid: 3fe45007-0de2-4905-96d7-fe351c81ae30
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpRemoveOptionValueV5, DhcpRemoveOptionValueV5 function [DHCP], dhcp.dhcpremoveoptionvaluev5, dhcpsapi/DhcpRemoveOptionValueV5
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
 - DhcpRemoveOptionValueV5
 - dhcpsapi/DhcpRemoveOptionValueV5
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
 - DhcpRemoveOptionValueV5
---

# DhcpRemoveOptionValueV5 function


## -description

The <b>DhcpRemoveOptionValueV5</b> function removes an option value from a scope defined on the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param Flags [in]

Specifies a bit flag that indicates whether or not the option is vendor-specific. If it is not, this parameter should be zero.

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

### -param OptionID [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that specifies the code for the option value to remove.

### -param ClassName [in]

Unicode string that specifies the DHCP  class name of the option value. This parameter is optional.

### -param VendorName [in]

Unicode string that specifies the vendor of the option. This parameter is optional, and should be <b>NULL</b> when <i>Flags</i> is not set to DHCP_FLAGS_OPTION_IS_VENDOR.

### -param ScopeInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a> structure that contains information describing the specific scope to remove the option value from.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetoptionvaluev5">DhcpSetOptionValueV5</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4removeoptionvalue">DhcpV4RemoveOptionValue</a>