---
UID: NF:dhcpsapi.DhcpV4FailoverGetScopeRelationship
title: DhcpV4FailoverGetScopeRelationship function (dhcpsapi.h)
description: Retrieves the failover relationship that is configured on a specified DHCPv4 scope.
helpviewer_keywords: ["DhcpV4FailoverGetScopeRelationship","DhcpV4FailoverGetScopeRelationship function [DHCP]","dhcp.dhcpv4failovergetscoperelationship","dhcpsapi/DhcpV4FailoverGetScopeRelationship"]
old-location: dhcp\dhcpv4failovergetscoperelationship.htm
tech.root: DHCP
ms.assetid: 795eb9ff-cc44-4567-b496-1bff559290b2
ms.date: 12/05/2018
ms.keywords: DhcpV4FailoverGetScopeRelationship, DhcpV4FailoverGetScopeRelationship function [DHCP], dhcp.dhcpv4failovergetscoperelationship, dhcpsapi/DhcpV4FailoverGetScopeRelationship
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
 - DhcpV4FailoverGetScopeRelationship
 - dhcpsapi/DhcpV4FailoverGetScopeRelationship
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
 - DhcpV4FailoverGetScopeRelationship
---

# DhcpV4FailoverGetScopeRelationship function


## -description

The <b>DhcpV4FailoverGetScopeRelationship</b> function retrieves the failover relationship that is configured on a specified DHCPv4 scope.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param ScopeId [in]

A <b>DHCP_IP_ADDRESS</b> field that contains the IPv4 scope address for which the relationship details are to be retrieved.

### -param pRelationship [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship">DHCP_FAILOVER_RELATIONSHIP</a> structure that contains information about the retrieved failover relationship which contains <b>scopeId</b> field in its <b>pScopes</b> member.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

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
<dt><b>ERROR_DHCP_FO_SCOPE_NOT_IN_RELATIONSHIP</b></dt>
</dl>
</td>
<td width="60%">
IPv4 subnet is not part of the failover relationship.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoveraddscopetorelationship">DhcpV4FailoverAddScopeToRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverdeletescopefromrelationship">DhcpV4FailoverDeleteScopeFromRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetscopestatistics">DhcpV4FailoverGetScopeStatistics</a>