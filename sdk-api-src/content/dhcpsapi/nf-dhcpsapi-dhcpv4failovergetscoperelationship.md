---
UID: NF:dhcpsapi.DhcpV4FailoverGetScopeRelationship
title: DhcpV4FailoverGetScopeRelationship function (dhcpsapi.h)
author: windows-sdk-content
description: Retrieves the failover relationship that is configured on a specified DHCPv4 scope.
old-location: dhcp\dhcpv4failovergetscoperelationship.htm
tech.root: DHCP
ms.assetid: 795eb9ff-cc44-4567-b496-1bff559290b2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DhcpV4FailoverGetScopeRelationship, DhcpV4FailoverGetScopeRelationship function [DHCP], dhcp.dhcpv4failovergetscoperelationship, dhcpsapi/DhcpV4FailoverGetScopeRelationship
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpV4FailoverGetScopeRelationship
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Pointer to a <a href="https://msdn.microsoft.com/b409b0ff-2fdc-416c-a7ce-2cba9cf75122">DHCP_FAILOVER_RELATIONSHIP</a> structure that contains information about the retrieved failover relationship which contains <b>scopeId</b> field in its <b>pScopes</b> member.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

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




<a href="https://msdn.microsoft.com/fc54b3dc-86b3-4a18-b05f-7152097f8d5b">DhcpV4FailoverAddScopeToRelationship</a>



<a href="https://msdn.microsoft.com/52420cc6-0a7b-499b-b7fe-35852a03adea">DhcpV4FailoverDeleteScopeFromRelationship</a>



<a href="https://msdn.microsoft.com/888945a8-5c07-440a-ad2d-2126342facda">DhcpV4FailoverGetScopeStatistics</a>
 

 

