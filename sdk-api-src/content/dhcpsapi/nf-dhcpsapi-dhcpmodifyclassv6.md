---
UID: NF:dhcpsapi.DhcpModifyClassV6
title: DhcpModifyClassV6 function (dhcpsapi.h)
description: Modifies a DHCPv6 user or vendor class defined on the server.
helpviewer_keywords: ["DhcpModifyClassV6","DhcpModifyClassV6 function [DHCP]","dhcp.dhcpmodifyclassv6","dhcpsapi/DhcpModifyClassV6"]
old-location: dhcp\dhcpmodifyclassv6.htm
tech.root: DHCP
ms.assetid: d98ea14e-d61a-4d1b-bd7f-9d8fdf81d092
ms.date: 12/05/2018
ms.keywords: DhcpModifyClassV6, DhcpModifyClassV6 function [DHCP], dhcp.dhcpmodifyclassv6, dhcpsapi/DhcpModifyClassV6
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
 - DhcpModifyClassV6
 - dhcpsapi/DhcpModifyClassV6
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
 - DhcpModifyClassV6
---

# DhcpModifyClassV6 function


## -description

The <b>DhcpModifyClassV6</b> function modifies a DHCPv6 user or vendor class defined on the server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ReservedMustBeZero [in]

Reserved. This value must be set to 0.

### -param ClassInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info_v6">DHCP_CLASS_INFO_V6</a> structure that contains the new information for the class.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info">DHCP_CLASS_INFO</a> structure provided in <i>ClassInfo</i> has null or invalid values for the <b>ClassName</b> or <b>ClassData</b> member (or both).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A class name could not be found that matches the provided information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCPv6 server's database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The new class name is currently in use, or the new class information is currently in use.

</td>
</tr>
</table>