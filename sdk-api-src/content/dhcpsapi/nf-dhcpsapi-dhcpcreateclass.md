---
UID: NF:dhcpsapi.DhcpCreateClass
title: DhcpCreateClass function (dhcpsapi.h)
description: Creates a custom option class.
helpviewer_keywords: ["DhcpCreateClass","DhcpCreateClass function [DHCP]","dhcp.dhcpcreateclass","dhcpsapi/DhcpCreateClass"]
old-location: dhcp\dhcpcreateclass.htm
tech.root: DHCP
ms.assetid: ae30baba-a2cd-4662-a62a-58b59d119dc4
ms.date: 12/05/2018
ms.keywords: DhcpCreateClass, DhcpCreateClass function [DHCP], dhcp.dhcpcreateclass, dhcpsapi/DhcpCreateClass
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
 - DhcpCreateClass
 - dhcpsapi/DhcpCreateClass
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
 - DhcpCreateClass
---

# DhcpCreateClass function


## -description

The <b>DhcpCreateClass</b> function creates a custom option class.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ReservedMustBeZero [in]

Reserved. This field must be set to zero.

### -param ClassInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info">DHCP_CLASS_INFO</a> structure that contains the specific option class data.

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
<dt><b>ERROR_DHCP_CLASS_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified class name is already defined on the DHCP server, or the class information is already in use..

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info">DHCP_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpdeleteclass">DhcpDeleteClass</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumclasses">DhcpEnumClasses</a>