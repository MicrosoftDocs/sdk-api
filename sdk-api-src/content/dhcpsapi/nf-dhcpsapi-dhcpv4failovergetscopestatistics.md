---
UID: NF:dhcpsapi.DhcpV4FailoverGetScopeStatistics
title: DhcpV4FailoverGetScopeStatistics function (dhcpsapi.h)
description: Retrieves the address usage statistics of a specific scope that is part of a failover relationship.
helpviewer_keywords: ["DhcpV4FailoverGetScopeStatistics","DhcpV4FailoverGetScopeStatistics function [DHCP]","dhcp.dhcpv4failovergetscopestatistics","dhcpsapi/DhcpV4FailoverGetScopeStatistics"]
old-location: dhcp\dhcpv4failovergetscopestatistics.htm
tech.root: DHCP
ms.assetid: 888945a8-5c07-440a-ad2d-2126342facda
ms.date: 12/05/2018
ms.keywords: DhcpV4FailoverGetScopeStatistics, DhcpV4FailoverGetScopeStatistics function [DHCP], dhcp.dhcpv4failovergetscopestatistics, dhcpsapi/DhcpV4FailoverGetScopeStatistics
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
 - DhcpV4FailoverGetScopeStatistics
 - dhcpsapi/DhcpV4FailoverGetScopeStatistics
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
 - DhcpV4FailoverGetScopeStatistics
---

# DhcpV4FailoverGetScopeStatistics function


## -description

The <b>DhcpV4FailoverGetScopeStatistics</b> function retrieves the address usage statistics of a specific scope that is part of a failover relationship.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param ScopeId [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the IPv4 scope address of the address usage statistics to retrieve.

### -param pStats [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_statistics">DHCP_FAILOVER_STATISTICS</a> structure that contains the address usage information for <i>scopeId</i>.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoveraddscopetorelationship">DhcpV4FailoverAddScopeToRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverdeletescopefromrelationship">DhcpV4FailoverDeleteScopeFromRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovergetscoperelationship">DhcpV4FailoverGetScopeRelationship</a>