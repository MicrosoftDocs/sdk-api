---
UID: NF:dhcpsapi.DhcpEnumOptions
title: DhcpEnumOptions function (dhcpsapi.h)
description: Returns an enumerated set of options stored on the DHCPv4 server.
helpviewer_keywords: ["DhcpEnumOptions","DhcpEnumOptions function [DHCP]","dhcp.dhcpenumoptions","dhcpsapi/DhcpEnumOptions"]
old-location: dhcp\dhcpenumoptions.htm
tech.root: DHCP
ms.assetid: b7a3afb2-cc5b-4181-997c-0cf3a049d091
ms.date: 12/05/2018
ms.keywords: DhcpEnumOptions, DhcpEnumOptions function [DHCP], dhcp.dhcpenumoptions, dhcpsapi/DhcpEnumOptions
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
 - DhcpEnumOptions
 - dhcpsapi/DhcpEnumOptions
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
 - DhcpEnumOptions
---

# DhcpEnumOptions function


## -description

The <b>DhcpEnumOptions</b> function returns an enumerated set of options stored on the DHCPv4 server.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IPv4 address of the DHCP server.

### -param ResumeHandle [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes worth of options are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth. 

The presence of additional enumerable data is indicated when this function returns ERROR_MORE_DATA. If no additional enumerable data is available on the DHCPv4 server, ERROR_NO_MORE_ITEMS is returned.

### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of options to return. If the number of remaining unenumerated options (in bytes) is less than this value, then that amount will be returned.

To retrieve all the option definitions for the default user and vendor class, set this parameter to 0xFFFFFFFF.

### -param Options [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_array">DHCP_OPTION_ARRAY</a> structure containing the returned options. If there are no options available on the DHCPv4 server, this parameter will return null.

### -param OptionsRead [out]

Pointer to a DWORD value that specifies the number of options returned in <i>Options</i>.

### -param OptionsTotal [out]

Pointer to a DWORD value that specifies the total number of remaining options stored on the DHCPv4 server.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
There are more elements available to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more elements left to enumerate.

</td>
</tr>
</table>

## -remarks

The caller of this function must free the memory pointed to by <i>Options</i> after the call completes.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_array">DHCP_OPTION_ARRAY</a>



<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreateoption">DhcpCreateOption</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpremoveoption">DhcpRemoveOption</a>