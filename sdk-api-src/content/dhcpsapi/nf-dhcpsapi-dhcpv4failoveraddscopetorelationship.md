---
UID: NF:dhcpsapi.DhcpV4FailoverAddScopeToRelationship
title: DhcpV4FailoverAddScopeToRelationship function (dhcpsapi.h)
description: Adds a DHCPv4 scope to the specified failover relationship.
helpviewer_keywords: ["DhcpV4FailoverAddScopeToRelationship","DhcpV4FailoverAddScopeToRelationship function [DHCP]","dhcp.dhcpv4failoveraddscopetorelationship","dhcpsapi/DhcpV4FailoverAddScopeToRelationship"]
old-location: dhcp\dhcpv4failoveraddscopetorelationship.htm
tech.root: DHCP
ms.assetid: fc54b3dc-86b3-4a18-b05f-7152097f8d5b
ms.date: 12/05/2018
ms.keywords: DhcpV4FailoverAddScopeToRelationship, DhcpV4FailoverAddScopeToRelationship function [DHCP], dhcp.dhcpv4failoveraddscopetorelationship, dhcpsapi/DhcpV4FailoverAddScopeToRelationship
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
 - DhcpV4FailoverAddScopeToRelationship
 - dhcpsapi/DhcpV4FailoverAddScopeToRelationship
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
 - DhcpV4FailoverAddScopeToRelationship
---

# DhcpV4FailoverAddScopeToRelationship function


## -description

The <b>DhcpV4FailoverAddScopeToRelationship</b> function adds a DHCPv4 scope to the specified failover relationship.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param pRelationship [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship">DHCP_FAILOVER_RELATIONSHIP</a> structure that contains both the scope information to add and the failover relationship to modify.

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
IPv4 scope is already part of another failover relationship.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_FO_RELATIONSHIP_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
Failover relationship doesn't exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_FO_MAX_ADD_SCOPES</b></dt>
</dl>
</td>
<td width="60%">
Number of scopes being added to the failover relationship exceeds the max number of scopes which can be added to a failover relationship at one time.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverdeletescopefromrelationship">DhcpV4FailoverDeleteScopeFromRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetscoperelationship">DhcpV4FailoverGetScopeRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetscopestatistics">DhcpV4FailoverGetScopeStatistics</a>