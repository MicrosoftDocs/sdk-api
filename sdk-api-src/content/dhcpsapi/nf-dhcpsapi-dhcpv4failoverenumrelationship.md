---
UID: NF:dhcpsapi.DhcpV4FailoverEnumRelationship
title: DhcpV4FailoverEnumRelationship function (dhcpsapi.h)
description: Enumerates all failover relationships present on the server.
helpviewer_keywords: ["DhcpV4FailoverEnumRelationship","DhcpV4FailoverEnumRelationship function [DHCP]","dhcp.dhcpv4failoverenumrelationship","dhcpsapi/DhcpV4FailoverEnumRelationship"]
old-location: dhcp\dhcpv4failoverenumrelationship.htm
tech.root: DHCP
ms.assetid: 81ef2af8-c1a9-44e7-857c-1591947609ed
ms.date: 12/05/2018
ms.keywords: DhcpV4FailoverEnumRelationship, DhcpV4FailoverEnumRelationship function [DHCP], dhcp.dhcpv4failoverenumrelationship, dhcpsapi/DhcpV4FailoverEnumRelationship
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - DhcpV4FailoverEnumRelationship
 - dhcpsapi/DhcpV4FailoverEnumRelationship
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
 - DhcpV4FailoverEnumRelationship
---

# DhcpV4FailoverEnumRelationship function


## -description

The <b>DhcpV4FailoverEnumRelationship</b> function enumerates all failover relationships present on the server.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param ResumeHandle [in, out]

Pointer to a  <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> structure that identifies this enumeration for use in subsequent calls to this function.

Initially, this value should be zero on input. If successful, the returned value should be used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 100, and 200 reservation elements are configured on the server, the resume handle can be used after the first 100 policies are retrieved to obtain the next 100 on a subsequent call.

### -param PreferredMaximum [in]

The maximum number of failover relationship elements to return in <i>pRelationship</i>. If <i>PreferredMaximum</i> is greater than the number of remaining non-enumerated policies on the server, the remaining number of  non-enumerated policies is returned.

### -param pRelationship [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship_array">DHCP_FAILOVER_RELATIONSHIP_ARRAY</a> structure that contains an array of the failover relationships available on the DHCP server. If no relationships are configured,<i></i> this value is <b>NULL</b>.

### -param RelationshipRead [out]

Pointer to a <b>DWORD</b> that specifies the number of failover relationship elements returned in <i>pRelationship</i>.

### -param RelationshipTotal [out]

Pointer to a <b>DWORD</b>  that specifies the number of failover relationships configured on the DHCP server that have not yet been enumerated.

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following. or an error code from <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovercreaterelationship">DhcpV4FailoverCreateRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverdeleterelationship">DhcpV4FailoverDeleteRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetrelationship">DhcpV4FailoverGetRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoversetrelationship">DhcpV4FailoverSetRelationship</a>