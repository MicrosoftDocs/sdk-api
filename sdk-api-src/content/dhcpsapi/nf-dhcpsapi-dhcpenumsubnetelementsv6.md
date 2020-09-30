---
UID: NF:dhcpsapi.DhcpEnumSubnetElementsV6
title: DhcpEnumSubnetElementsV6 function (dhcpsapi.h)
description: The DhcpEnumSubnetElementsV6 function returns an enumerated list of elements for a specific DHCP subnet.
helpviewer_keywords: ["DhcpEnumSubnetElementsV6","DhcpEnumSubnetElementsV6 function [DHCP]","dhcp.dhcpenumsubnetelementsv6","dhcpsapi/DhcpEnumSubnetElementsV6"]
old-location: dhcp\dhcpenumsubnetelementsv6.htm
tech.root: DHCP
ms.assetid: 72f40256-7f49-41f3-ac31-d863cd6383db
ms.date: 12/05/2018
ms.keywords: DhcpEnumSubnetElementsV6, DhcpEnumSubnetElementsV6 function [DHCP], dhcp.dhcpenumsubnetelementsv6, dhcpsapi/DhcpEnumSubnetElementsV6
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
 - DhcpEnumSubnetElementsV6
 - dhcpsapi/DhcpEnumSubnetElementsV6
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
 - DhcpEnumSubnetElementsV6
---

# DhcpEnumSubnetElementsV6 function


## -description

The <b>DhcpEnumSubnetElementsV6</b> function returns an enumerated list of elements for a specific DHCP subnet.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

DHCP_IPV6_ADDRESS value that specifies the subnet whose elements will be enumerated.

### -param EnumElementType [in]

DHCP_SUBNET_ELEMENT_TYPE_V6 enumeration value that indicates the type of subnet element to enumerate.

### -param ResumeHandle [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes worth of subnet elements  are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth.

### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of subnet elements to return. If the number of remaining unenumerated options (in bytes) is less than this value, then that amount will be returned.

### -param EnumElementInfo [out]

Pointer to a DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6 structure containing an enumerated list of all elements available for the specified subnet. If no elements are available for enumeration, this value will be null.

### -param ElementsRead [out]

Pointer to a DWORD value that specifies the number of subnet elements returned in <i>EnumElementInfo</i>.

### -param ElementsTotal [out]

Pointer to a DWORD value that specifies the total number of elements for the specified subnet.

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