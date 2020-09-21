---
UID: NF:dhcpsapi.DhcpV4SetOptionValue
title: DhcpV4SetOptionValue function (dhcpsapi.h)
description: Sets information for a specific option value on the DHCP server. This function extends the functionality provided by DhcpSetOptionValueV5 by allowing the caller to specify a policy for the option.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpV4SetOptionValue","DhcpV4SetOptionValue function [DHCP]","dhcp.dhcpv4setoptionvalue","dhcpsapi/DhcpV4SetOptionValue"]
old-location: dhcp\dhcpv4setoptionvalue.htm
tech.root: DHCP
ms.assetid: cf8141cc-8cf3-4932-b13a-e276dcdeb825
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpV4SetOptionValue, DhcpV4SetOptionValue function [DHCP], dhcp.dhcpv4setoptionvalue, dhcpsapi/DhcpV4SetOptionValue
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - DhcpV4SetOptionValue
 - dhcpsapi/DhcpV4SetOptionValue
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
 - DhcpV4SetOptionValue
---

# DhcpV4SetOptionValue function


## -description

The <b>DhcpV4SetOptionValue</b> function  sets information for a specific option value on the DHCP server. This function extends the functionality provided by <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetoptionvaluev5">DhcpSetOptionValueV5</a> by allowing the caller to specify a policy for the option.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param Flags [in]

Indicates whether the option is for a specific or default vendor.

<table>
<tr>
<th>Flags</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The option value is retrieved for a default vendor.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The option value is retrieved for a specific vendor. The vendor is in <i>VendorName</i>.

</td>
</tr>
</table>

### -param OptionId [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> structure that specifies the unique option code for the option value to retrieve. A complete list of standard DHCP and BOOTP option codes can be found at <a href="http://www.ietf.org/rfc/rfc2132.txt">http://www.ietf.org/rfc/rfc2132.txt</a>

### -param PolicyName [in, optional]

A null-terminated Unicode string that represents the name of the policy inside the subnet of the option value to set. The subnet is identified by the <b>SubnetScopeInfo</b> member of <i>ScopeInfo</i>.

### -param VendorName [in, optional]

A null-terminated Unicode string that represents the vendor  of the option. This parameter is optional, and should be <b>NULL</b> when <i>Flags</i> is not <b>DHCP_FLAGS_OPTION_IS_VENDOR</b>. If the vendor is not specified, the option value is set for the default vendor.

### -param ScopeInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a> structure that contains information on the scope of the option value to set.

### -param OptionValue [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_data">DHCP_OPTION_DATA</a> structure that contains the data value corresponding to the DHCP option code specified by <i>OptionID</i>.

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The class name being used is unknown or incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_POLICY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified policy name does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition does not exist on the DHCP server database.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4getalloptionvalues">DhcpV4GetAllOptionValues</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4getoptionvalue">DhcpV4GetOptionValue</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4removeoptionvalue">DhcpV4RemoveOptionValue</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setoptionvalues">DhcpV4SetOptionValues</a>