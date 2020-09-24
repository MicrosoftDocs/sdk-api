---
UID: NF:dhcpsapi.DhcpGetClassInfo
title: DhcpGetClassInfo function (dhcpsapi.h)
description: The DhcpGetClassInfo function returns the user or vendor class information configured on a specific DHCP server.
helpviewer_keywords: ["DhcpGetClassInfo","DhcpGetClassInfo function [DHCP]","dhcp.dhcpgetclassinfo","dhcpsapi/DhcpGetClassInfo"]
old-location: dhcp\dhcpgetclassinfo.htm
tech.root: DHCP
ms.assetid: c38a593f-60f0-41c7-83a8-bbec9b79dfac
ms.date: 12/05/2018
ms.keywords: DhcpGetClassInfo, DhcpGetClassInfo function [DHCP], dhcp.dhcpgetclassinfo, dhcpsapi/DhcpGetClassInfo
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
 - DhcpGetClassInfo
 - dhcpsapi/DhcpGetClassInfo
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
 - DhcpGetClassInfo
---

# DhcpGetClassInfo function


## -description

The <b>DhcpGetClassInfo</b> function returns the user or vendor class information configured on a specific DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ReservedMustBeZero [in]

Reserved. This parameter must be set to 0.

### -param PartialClassInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info">DHCP_CLASS_INFO</a> structure that contains data provided by the caller for the following members, with all other fields initialized. 

<ul>
<li><b>ClassName</b></li>
<li><b>ClassData</b></li>
<li><b>ClassDataLength</b></li>
</ul>
These fields must not be null.

### -param FilledClassInfo [out]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info">DHCP_CLASS_INFO</a> structure returned after lookup that contains the complete class information.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

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
The <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info">DHCP_CLASS_INFO</a> structure provided in <i>PartialClassInfo</i> has null or zero values for one or more of the required members.

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
</table>

## -remarks

A DHCP class is a specific category of client, defined either by the vendor or by a user. An example of a vendor-defined class would be all Windows 8 clients, with Microsoft as the vendor. A user-defined class consists of those clients with specific attributes selected by a user or administrator, such as all laptops or clients that support wireless connections.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info">DHCP_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreateclass">DhcpCreateClass</a>