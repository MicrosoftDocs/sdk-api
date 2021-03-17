---
UID: NF:dhcpsapi.DhcpEnumFilterV4
title: DhcpEnumFilterV4 function (dhcpsapi.h)
description: Enumerates all of the filter records from the DHCP server's allow or deny list.
helpviewer_keywords: ["DhcpEnumFilterV4","DhcpEnumFilterV4 function [DHCP]","dhcp.dhcpenumfilterv4","dhcpsapi/DhcpEnumFilterV4"]
old-location: dhcp\dhcpenumfilterv4.htm
tech.root: DHCP
ms.assetid: a861b34a-19cc-4732-bb38-6b0643319640
ms.date: 12/05/2018
ms.keywords: DhcpEnumFilterV4, DhcpEnumFilterV4 function [DHCP], dhcp.dhcpenumfilterv4, dhcpsapi/DhcpEnumFilterV4
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
 - DhcpEnumFilterV4
 - dhcpsapi/DhcpEnumFilterV4
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
 - DhcpEnumFilterV4
---

# DhcpEnumFilterV4 function


## -description

The <b>DhcpEnumFilterV4</b> function enumerates all of the filter records from the DHCP server's allow or deny list.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ResumeHandle [in, out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_addr_pattern">DHCP_ADDR_PATTERN</a> structure that identifies the enumeration operation. Initially this parameter must be set to zero (0), with a successful call returning the address/pattern value used for subsequent enumeration requests.

### -param PreferredMaximum [in]

A DWORD value that specifies the preferred maximum number of bytes to return. If the number of remaining unenumerated filter information size is less than this value, then all the filters configured on the particular list on the DHCP server are returned. The maximum value for this is 64 (kilobytes), and the minimum value is 1 (kilobyte).

### -param ListType [in]

A <a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_filter_list_type">DHCP_FILTER_LIST_TYPE</a> that specifies the list of filters to be enumerated.

### -param EnumFilterInfo [out]

Pointer to the address of an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_filter_enum_info">DHCP_FILTER_ENUM_INFO</a> structures that contain the returned link-layer filter information configured on the DHCP server.

### -param ElementsRead [out]

Pointer to a <b>DWORD</b> value that specifies the number of link-layer filter entries returned in <i>EnumFilterInfo</i>.

### -param ElementsTotal [out]

Pointer to a <b>DWORD</b> value that specifies the number of link-layer filter entries defined on the DHCP server that have not yet been enumerated.

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
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server's database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
There are no more elements available for enumeration.

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

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_filter_enum_info">DHCP_FILTER_ENUM_INFO</a>



<a href="/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_filter_list_type">DHCP_FILTER_LIST_TYPE</a>