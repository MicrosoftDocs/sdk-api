---
UID: NF:dhcpsapi.DhcpEnumClasses
title: DhcpEnumClasses function (dhcpsapi.h)
description: Enumerates the user or vendor classes configured for the DHCP server.
helpviewer_keywords: ["DhcpEnumClasses","DhcpEnumClasses function [DHCP]","dhcp.dhcpenumclasses","dhcpsapi/DhcpEnumClasses"]
old-location: dhcp\dhcpenumclasses.htm
tech.root: DHCP
ms.assetid: 93f37424-1a81-477e-85da-359885e94349
ms.date: 12/05/2018
ms.keywords: DhcpEnumClasses, DhcpEnumClasses function [DHCP], dhcp.dhcpenumclasses, dhcpsapi/DhcpEnumClasses
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
 - DhcpEnumClasses
 - dhcpsapi/DhcpEnumClasses
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
 - DhcpEnumClasses
---

# DhcpEnumClasses function


## -description

The <b>DhcpEnumClasses</b> function enumerates the  user or vendor classes configured for the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ReservedMustBeZero [in]

Reserved. This field must be set to zero.

### -param ResumeHandle [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 100 classes, and 200 classes are stored on the server, the resume handle can be used after the first 100 classes are retrieved to obtain the next 100 on a subsequent call, and so forth.

### -param PreferredMaximum [in]

Specifies the preferred maximum number of classes to return. If the number of remaining unenumerated classes is less than this value, then that amount will be returned. To retrieve all classes available on the DHCP server, set this parameter to 0xFFFFFFFF.

### -param ClassInfoArray [out]

Pointer to a  <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info_array">DHCP_CLASS_INFO_ARRAY</a> structure that contains the returned classes. If there are no classes available on the DHCP server, this parameter will return null.

### -param nRead [out]

Pointer to a DWORD value that specifies the number of classes returned in <i>ClassInfoArray</i>.

### -param nTotal [out]

Pointer to a DWORD value that specifies the total number of classes stored on the DHCP server.

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
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info_array">DHCP_CLASS_INFO_ARRAY</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreateclass">DhcpCreateClass</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpdeleteclass">DhcpDeleteClass</a>