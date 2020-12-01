---
UID: NF:dhcpsapi.DhcpV4SetOptionValues
title: DhcpV4SetOptionValues function (dhcpsapi.h)
description: Sets option codes and their associated data values for a specific scope defined on the DHCP server. This function extends the functionality provided by DhcpSetOptionValuesV5 by allowing the caller to specify a policy for the options.
helpviewer_keywords: ["DhcpV4SetOptionValues","DhcpV4SetOptionValues function [DHCP]","dhcp.dhcpv4setoptionvalues","dhcpsapi/DhcpV4SetOptionValues"]
old-location: dhcp\dhcpv4setoptionvalues.htm
tech.root: DHCP
ms.assetid: 8c50af53-8298-401e-826e-0fb1d1410499
ms.date: 12/05/2018
ms.keywords: DhcpV4SetOptionValues, DhcpV4SetOptionValues function [DHCP], dhcp.dhcpv4setoptionvalues, dhcpsapi/DhcpV4SetOptionValues
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
 - DhcpV4SetOptionValues
 - dhcpsapi/DhcpV4SetOptionValues
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
 - DhcpV4SetOptionValues
---

# DhcpV4SetOptionValues function


## -description

The <b>DhcpV4SetOptionValues</b> function  sets option codes and their associated data values for a specific scope defined on the DHCP server. This function extends the functionality provided by <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetoptionvaluesv5">DhcpSetOptionValuesV5</a> by allowing the caller to specify a policy for the options.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param Flags [in]

Reserved. Must be 0.

### -param PolicyName [in, optional]

A null-terminated Unicode string that represents the name of the policy inside the subnet of the option value to set. The subnet is identified by the <b>SubnetScopeInfo</b> member of <i>ScopeInfo</i>.

### -param VendorName [in, optional]

A null-terminated Unicode string that represents the vendor  of the option. This parameter is optional, and if <b>NULL</b>, the option value is set for the default vendor.

### -param ScopeInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a> structure that contains information describing the DHCP scope of the option values to set. This parameter specifies whether the option value is set for the default, server, or scope level, or for an IPv4 reservation.

### -param OptionValues [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value_array">DHCP_OPTION_VALUE_ARRAY</a> structure that contains a list of option codes and the corresponding data value that will be set.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_NOT_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP client is not a reserved client.

</td>
</tr>
</table>

## -remarks

<i>OptionValues</i> and its member, <b>Values</b>, should be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4getalloptionvalues">DhcpV4GetAllOptionValues</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4getoptionvalue">DhcpV4GetOptionValue</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4removeoptionvalue">DhcpV4RemoveOptionValue</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setoptionvalue">DhcpV4SetOptionValue</a>