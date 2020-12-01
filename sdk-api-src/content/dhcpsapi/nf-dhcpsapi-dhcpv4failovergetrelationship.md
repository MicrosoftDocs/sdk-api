---
UID: NF:dhcpsapi.DhcpV4FailoverGetRelationship
title: DhcpV4FailoverGetRelationship function (dhcpsapi.h)
description: Retrieves relationship details for a specific relationship name.
helpviewer_keywords: ["DhcpV4FailoverGetRelationship","DhcpV4FailoverGetRelationship function [DHCP]","dhcp.dhcpv4failovergetrelationship","dhcpsapi/DhcpV4FailoverGetRelationship"]
old-location: dhcp\dhcpv4failovergetrelationship.htm
tech.root: DHCP
ms.assetid: b637d1e8-8c61-4382-a5ec-3d5395433f86
ms.date: 12/05/2018
ms.keywords: DhcpV4FailoverGetRelationship, DhcpV4FailoverGetRelationship function [DHCP], dhcp.dhcpv4failovergetrelationship, dhcpsapi/DhcpV4FailoverGetRelationship
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
 - DhcpV4FailoverGetRelationship
 - dhcpsapi/DhcpV4FailoverGetRelationship
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
 - DhcpV4FailoverGetRelationship
---

# DhcpV4FailoverGetRelationship function


## -description

The <b>DhcpV4FailoverGetRelationship</b> function retrieves relationship details for a specific relationship name.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param pRelationshipName [in]

Pointer to a null-terminated Unicode string which represents the name of the relationship to retrieve.

### -param pRelationship [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship">DHCP_FAILOVER_RELATIONSHIP</a> structure that contains information about the retrieved failover relationship.

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
<dt><b>ERROR_DHCP_FO_RELATIONSHIP_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The failover relationship does not exist.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failovercreaterelationship">DhcpV4FailoverCreateRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverdeleterelationship">DhcpV4FailoverDeleteRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoverenumrelationship">DhcpV4FailoverEnumRelationship</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4failoversetrelationship">DhcpV4FailoverSetRelationship</a>