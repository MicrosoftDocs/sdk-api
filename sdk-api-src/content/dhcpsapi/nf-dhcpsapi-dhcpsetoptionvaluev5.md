---
UID: NF:dhcpsapi.DhcpSetOptionValueV5
title: DhcpSetOptionValueV5 function (dhcpsapi.h)
description: The DhcpSetOptionValueV5 function sets information for a specific option value on the DHCP server. This function extends the functionality provided by DhcpSetOptionValue by allowing the caller to specify a class and/or vendor for the option.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpSetOptionValueV5","DhcpSetOptionValueV5 function [DHCP]","dhcp.dhcpsetoptionvaluev5","dhcpsapi/DhcpSetOptionValueV5"]
old-location: dhcp\dhcpsetoptionvaluev5.htm
tech.root: DHCP
ms.assetid: 05e7930f-e5c1-42e7-a693-f9852cda9494
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpSetOptionValueV5, DhcpSetOptionValueV5 function [DHCP], dhcp.dhcpsetoptionvaluev5, dhcpsapi/DhcpSetOptionValueV5
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
 - DhcpSetOptionValueV5
 - dhcpsapi/DhcpSetOptionValueV5
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
 - DhcpSetOptionValueV5
---

# DhcpSetOptionValueV5 function


## -description

The <b>DhcpSetOptionValueV5</b> function sets 
    information for a specific option value on the DHCP server. This function extends the functionality provided by 
    <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetoptionvalue">DhcpSetOptionValue</a> by allowing the caller to 
    specify a class and/or vendor for the option.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param Flags [in]

Specifies a bit flag that indicates whether or not the option is vendor-specific. If it is not, this 
      parameter should be 0.

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

DHCP_OPTION_ID value that contains the unique option ID number (also called an "option code") of the 
      option being set. Many of these option ID numbers are defined; a complete list of standard DHCP and BOOTP 
      option codes can be found at 
      <a href="http://www.ietf.org/rfc/rfc2132.txt">http://www.ietf.org/rfc/rfc2132.txt</a>.

### -param ClassName [in, optional]

Unicode string that specifies the DHCP  class  of the option. This parameter is optional.

### -param VendorName [in, optional]

Unicode string that specifies the vendor of the option. This parameter is optional, and should be <b>NULL</b> 
      when <i>Flags</i> is not set to DHCP_FLAGS_OPTION_IS_VENDOR.

### -param ScopeInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a> 
      structure that contains information describing the DHCP scope this option value will be set on.

### -param OptionValue [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data">DHCP_OPTION_DATA</a> structure that 
      contains the data value corresponding to the DHCP option code specified by 
      <i>OptionID</i>.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns 
       one of the 
       <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data">DHCP_OPTION_DATA</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setoptionvalue">DhcpV4SetOptionValue</a>