---
UID: NF:dhcpsapi.DhcpEnumOptionsV6
title: DhcpEnumOptionsV6 function (dhcpsapi.h)
description: The DhcpEnumOptionsV6 function returns an enumerated list of DHCP options for a given class and/or vendor.
helpviewer_keywords: ["DHCP_FLAGS_OPTION_IS_VENDOR","DhcpEnumOptionsV6","DhcpEnumOptionsV6 function [DHCP]","dhcp.dhcpenumoptionsv6","dhcpsapi/DhcpEnumOptionsV6"]
old-location: dhcp\dhcpenumoptionsv6.htm
tech.root: DHCP
ms.assetid: 23abdca3-2241-4766-81c2-a4e8841b89fb
ms.date: 12/05/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpEnumOptionsV6, DhcpEnumOptionsV6 function [DHCP], dhcp.dhcpenumoptionsv6, dhcpsapi/DhcpEnumOptionsV6
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
 - DhcpEnumOptionsV6
 - dhcpsapi/DhcpEnumOptionsV6
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
 - DhcpEnumOptionsV6
---

# DhcpEnumOptionsV6 function


## -description

The <b>DhcpEnumOptionsV6</b> function returns an enumerated list of DHCP options for a given class and/or vendor.

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

### -param ClassName [in]

Unicode string that contains the name of the class whose options will be enumerated.

### -param VendorName [in]

Unicode string that contains the name of the vendor for the class. This parameter is optional.

### -param ResumeHandle [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes worth of options are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth.

### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of options to return. If the number of remaining unenumerated options (in bytes) is less than this value, then that amount will be returned.

### -param Options [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_array">DHCP_OPTION_ARRAY</a> structure containing the returned options. If there are no options available on the DHCP server, this parameter will return null.

### -param OptionsRead [out]

Pointer to a DWORD value that specifies the number of options returned in <i>Options</i>.

### -param OptionsTotal [out]

Pointer to a DWORD value that specifies the total number of options stored on the DHCP server.

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