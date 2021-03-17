---
UID: NF:dhcpsapi.DhcpGetOptionValueV6
title: DhcpGetOptionValueV6 function (dhcpsapi.h)
description: Retrieves the option value for a specific option defined on the DHCPv6 server for a specific user or vendor class.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpGetOptionValueV6","DhcpGetOptionValueV6 function [DHCP]","dhcp.dhcpgetoptionvaluev6","dhcpsapi/DhcpGetOptionValueV6"]
old-location: dhcp\dhcpgetoptionvaluev6.htm
tech.root: DHCP
ms.assetid: 62ad5e0f-d5e2-42d2-9e09-a7f2736ee7ab
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpGetOptionValueV6, DhcpGetOptionValueV6 function [DHCP], dhcp.dhcpgetoptionvaluev6, dhcpsapi/DhcpGetOptionValueV6
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
 - DhcpGetOptionValueV6
 - dhcpsapi/DhcpGetOptionValueV6
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
 - DhcpGetOptionValueV6
---

# DhcpGetOptionValueV6 function


## -description

The <b>DhcpGetOptionValueV6</b> function retrieves the option value for a specific option defined on the DHCPv6 server for a specific user or vendor class.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IPv6 address or hostname of the DHCPv6 server.

### -param Flags [in]

Flag value that indicates whether the option is for a specific or default vendor class.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The option value is retrieved for a default vendor class.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The option value is retrieved for a specific vendor class. The vendor name is supplied in <i>VendorName</i>.

</td>
</tr>
</table>

### -param OptionID [in]

<b>DHCP_OPTION_ID</b> value that specifies the option identifier for the option being retrieved.

### -param ClassName [in]

Pointer to a null-terminated Unicode string that contains the name of the user class for which the option value is being requested. This parameter is optional.

### -param VendorName [in]

Pointer to a null-terminated Unicode string that contains the name of the vendor class for which the option value is being requested. This parameter is optional; if no value is specified, the default vendor class is assumed.

### -param ScopeInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info6">DHCP_OPTION_SCOPE_INFO6</a> structure that contains information about the DHCPv6 scope for which the option is value is requested. Specifically, it defines whether the option is being retrieved for the default, server, or scope level, or for a specific IPv6 reservation.

### -param OptionValue [out]

Pointer to the address of a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value">DHCP_OPTION_VALUE</a> structure returned by the operation, and which contains the option value corresponding to <i>OptionID</i>.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client who is not a member of the "DHCP Administrators" security group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the specified file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified subnet is not defined on the DHCPv6 server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option is not defined at the specified level on the DHCPv6 server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_NOT_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The reserved IPv6 client is not defined on the DHCPv6 server.

</td>
</tr>
</table>

## -remarks

The caller of this function must release the memory pointed to by <i>OptionValue</i>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info6">DHCP_OPTION_SCOPE_INFO6</a>