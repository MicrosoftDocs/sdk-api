---
UID: NF:dhcpsapi.DhcpSetOptionValuesV5
title: DhcpSetOptionValuesV5 function (dhcpsapi.h)
description: Sets option codes and their associated data values for a specific scope defined on the DHCP server. This function extends the functionality provided by DhcpSetOptionValues by allowing the caller to specify a class and/or vendor for the options.
helpviewer_keywords: ["DhcpSetOptionValuesV5","DhcpSetOptionValuesV5 function [DHCP]","dhcp.dhcpsetoptionvaluesv5","dhcpsapi/DhcpSetOptionValuesV5"]
old-location: dhcp\dhcpsetoptionvaluesv5.htm
tech.root: DHCP
ms.assetid: 53549094-d642-4635-9dd6-5ce16d6be08a
ms.date: 12/05/2018
ms.keywords: DhcpSetOptionValuesV5, DhcpSetOptionValuesV5 function [DHCP], dhcp.dhcpsetoptionvaluesv5, dhcpsapi/DhcpSetOptionValuesV5
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
 - DhcpSetOptionValuesV5
 - dhcpsapi/DhcpSetOptionValuesV5
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
 - DhcpSetOptionValuesV5
---

# DhcpSetOptionValuesV5 function


## -description

The <b>DhcpSetOptionValuesV5</b> function sets option codes and their associated data values for a specific scope defined on the DHCP server. This function extends the functionality provided by <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetoptionvalues">DhcpSetOptionValues</a> by allowing the caller to specify a class and/or vendor for the options.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IPv4 address of the DHCP server.

### -param Flags [in]

This parameter must be set to 0 and ignored upon receipt.

### -param ClassName [in]

Unicode string that specifies the DHCP  class  of the options. This parameter is optional.

### -param VendorName [in]

Unicode string that specifies the vendor of the options. If no vendor class is specified, then the option value is set for the default vendor class. This parameter is optional.

### -param ScopeInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a> structure that contains information describing the DHCP scope these option values will be set on. This parameter indicates whether the option value is set for the default, server, or scope level, or for an IPv4 reservation.

### -param OptionValues [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value_array">DHCP_OPTION_VALUE_ARRAY</a> structure that contains a list of option codes and the corresponding data value that will be set for them.

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
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet does not exist on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition could not be found in the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_NOT_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP client is not an IPv4 reserved client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified class name cannot be found in the DHCP server database.

</td>
</tr>
</table>

## -remarks

The caller of this function must release the memory pointed to by <i>OptionValues</i> after the call completes.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value_array">DHCP_OPTION_VALUE_ARRAY</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetoptionvaluesv5">DhcpSetOptionValueV5</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetoptionvalues">DhcpSetOptionValues</a>