---
UID: NF:dhcpsapi.DhcpV4FailoverCreateRelationship
title: DhcpV4FailoverCreateRelationship function (dhcpsapi.h)
description: Creates a new DHCPv4 failover relationship between two servers.
helpviewer_keywords: ["DhcpV4FailoverCreateRelationship","DhcpV4FailoverCreateRelationship function [DHCP]","dhcp.dhcpv4failovercreaterelationship","dhcpsapi/DhcpV4FailoverCreateRelationship"]
old-location: dhcp\dhcpv4failovercreaterelationship.htm
tech.root: DHCP
ms.assetid: 6e360dd4-b4a0-4652-8754-17c3c284271c
ms.date: 12/05/2018
ms.keywords: DhcpV4FailoverCreateRelationship, DhcpV4FailoverCreateRelationship function [DHCP], dhcp.dhcpv4failovercreaterelationship, dhcpsapi/DhcpV4FailoverCreateRelationship
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
 - DhcpV4FailoverCreateRelationship
 - dhcpsapi/DhcpV4FailoverCreateRelationship
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
 - DhcpV4FailoverCreateRelationship
---

# DhcpV4FailoverCreateRelationship function


## -description

The <b>DhcpV4FailoverCreateRelationship</b> function creates a new DHCPv4 failover relationship between two servers.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param pRelationship [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship">DHCP_FAILOVER_RELATIONSHIP</a> structure that contains information about the DHCPv4 failover relationship to create.

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

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
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
IPv4 scope doesn't exist on the DHCPv4 server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_FO_SCOPE_ALREADY_IN_RELATIONSHIP</b></dt>
</dl>
</td>
<td width="60%">
IPv4 is already part of another failover relationship.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_FO_RELATIONSHIP_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
A failover relationship with the same name already exists on DHCPv4 server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_FO_RELATIONSHIP_NAME_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The failover relationship name is longer than the expected length.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_FO_MAX_RELATIONSHIPS</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of allowed failover relationship configured on the DHCP server has exceeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverdeleterelationship">DhcpV4FailoverDeleteRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverenumrelationship">DhcpV4FailoverEnumRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetrelationship">DhcpV4FailoverGetRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoversetrelationship">DhcpV4FailoverSetRelationship</a>