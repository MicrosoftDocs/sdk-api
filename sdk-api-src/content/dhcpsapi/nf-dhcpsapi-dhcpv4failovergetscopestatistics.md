---
UID: NF:dhcpsapi.DhcpV4FailoverGetScopeStatistics
title: DhcpV4FailoverGetScopeStatistics function
author: windows-sdk-content
description: Retrieves the address usage statistics of a specific scope that is part of a failover relationship.
old-location: dhcp\dhcpv4failovergetscopestatistics.htm
old-project: DHCP
ms.assetid: 888945a8-5c07-440a-ad2d-2126342facda
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DhcpV4FailoverGetScopeStatistics, DhcpV4FailoverGetScopeStatistics function [DHCP], dhcp.dhcpv4failovergetscopestatistics, dhcpsapi/DhcpV4FailoverGetScopeStatistics
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpV4FailoverGetScopeStatistics
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpV4FailoverGetScopeStatistics function


## -description


The <b>DhcpV4FailoverGetScopeStatistics</b> function retrieves the address usage statistics of a specific scope that is part of a failover relationship.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param ScopeId

TBD


### -param pStats [out]

Pointer to a <a href="https://msdn.microsoft.com/a06d873c-fc82-40c1-be3e-45f24328897d">DHCP_FAILOVER_STATISTICS</a> structure that contains the address usage information for <i>scopeId</i>.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

#### - scopeId [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that contains the IPv4 scope address of the address usage statistics to retrieve.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fc54b3dc-86b3-4a18-b05f-7152097f8d5b">DhcpV4FailoverAddScopeToRelationship</a>



<a href="https://msdn.microsoft.com/52420cc6-0a7b-499b-b7fe-35852a03adea">DhcpV4FailoverDeleteScopeFromRelationship</a>



<a href="https://msdn.microsoft.com/795eb9ff-cc44-4567-b496-1bff559290b2">DhcpV4FailoverGetScopeRelationship</a>
 

 

