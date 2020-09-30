---
UID: NF:dhcpsapi.DhcpEnumOptionValuesV6
title: DhcpEnumOptionValuesV6 function (dhcpsapi.h)
description: The DhcpEnumOptionValuesV6 function returns an enumerated list of option values (the option data and the associated ID number) for a specific scope within a given class.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpEnumOptionValuesV6","DhcpEnumOptionValuesV6 function [DHCP]","dhcp.dhcpenumoptionvaluesv6","dhcpsapi/DhcpEnumOptionValuesV6"]
old-location: dhcp\dhcpenumoptionvaluesv6.htm
tech.root: DHCP
ms.assetid: c63c8e41-5ca6-4989-9674-9c5c0f516af7
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpEnumOptionValuesV6, DhcpEnumOptionValuesV6 function [DHCP], dhcp.dhcpenumoptionvaluesv6, dhcpsapi/DhcpEnumOptionValuesV6
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
 - DhcpEnumOptionValuesV6
 - dhcpsapi/DhcpEnumOptionValuesV6
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
 - DhcpEnumOptionValuesV6
---

# DhcpEnumOptionValuesV6 function


## -description

The <b>DhcpEnumOptionValuesV6</b> function returns an enumerated list of option values (the option data and the associated ID number) for a specific scope within a given class.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param Flags [in]

Specifies a bit flag that indicates whether or not the option is vendor specific. If it is not vendor specific, this parameter should be 0.

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

### -param ClassName [in]

Unicode string that contains the name of the class whose scope's option values will be enumerated.

### -param VendorName [in]

Unicode string that contains the name of the vendor for the class. This parameter is optional.

### -param ScopeInfo [in]

DHCP_OPTION_SCOPE_INFO6 structure that contains the  scope for which the option values are defined.

### -param ResumeHandle [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes worth of option values  are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth.

### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of option values to return. If the number of remaining unenumerated options (in bytes) is less than this value, then that amount will be returned.

### -param OptionValues [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value_array">DHCP_OPTION_VALUE_ARRAY</a> structure that contains the enumerated option values returned for the specified scope. If there are no option values available for this scope on the DHCP server, this parameter will return null.

### -param OptionsRead [out]

Pointer to a DWORD value that specifies the number of option values returned in <i>OptionValues</i>.

### -param OptionsTotal [out]

Pointer to a DWORD value that specifies the total number of option values for this scope stored on the DHCP server.

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
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more items to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More data is available to enumerate.

</td>
</tr>
</table>