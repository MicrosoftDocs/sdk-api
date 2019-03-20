---
UID: NF:dhcpsapi.DhcpV4CreatePolicy
title: DhcpV4CreatePolicy function (dhcpsapi.h)
author: windows-sdk-content
description: Creates a new policy on the DHCP Server.
old-location: dhcp\dhcpv4createpolicy.htm
tech.root: DHCP
ms.assetid: c42e9c64-d028-4489-82dc-85ce9a6d6c09
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DhcpV4CreatePolicy, DhcpV4CreatePolicy function [DHCP], dhcp.dhcpv4createpolicy, dhcpsapi/DhcpV4CreatePolicy
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
 - DhcpV4CreatePolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpV4CreatePolicy function


## -description


The <b>DhcpV4CreatePolicy</b> function creates a new policy on the DHCP Server.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param pPolicy [in]

Pointer to a <a href="https://msdn.microsoft.com/7e62d2f3-275a-45ab-baab-648fe135d0fc">DHCP_POLICY</a> structure that contains the parameters of the policy to create.


## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_RANGE_INVALID_IN_SERVER_POLICY</b></dt>
</dl>
</td>
<td width="60%">
A policy range has been specified for a server level policy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_INVALID_POLICY_EXPRESSION</b></dt>
</dl>
</td>
<td width="60%">
The specified conditions or expressions of the policy are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_POLICY_RANGE_BAD</b></dt>
</dl>
</td>
<td width="60%">
The specified policy IP range is not contained within the IP address range of the scope or the specified policy IP range is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_POLICY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified policy name exists at the specified level (server or scope).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_POLICY_RANGE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified policy IP range overlaps with the policy IP ranges of an existing policy at the specified scope.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_INVALID_PROCESSING_ORDER</b></dt>
</dl>
</td>
<td width="60%">
The specified processing order is greater than the maximum processing order of the existing policies at the specified level (server or scope).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The vendor class or user class reference in the conditions of the policy does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameters were invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/43ec0634-6a4b-4d70-98d1-410b33a7cb17">DhcpV4AddPolicyRange</a>



<a href="https://msdn.microsoft.com/94e6ad23-3e38-4ee2-bc3a-8d7ff1b21eca">DhcpV4DeletePolicy</a>



<a href="https://msdn.microsoft.com/c3915699-f60d-495c-81df-85dc6fe2657c">DhcpV4EnumPolicies</a>



<a href="https://msdn.microsoft.com/a6112bf8-5c1f-4f33-ba1f-b4903cc6befa">DhcpV4GetPolicy</a>



<a href="https://msdn.microsoft.com/a622d83c-bb18-4482-be8d-fdd96382a5e1">DhcpV4QueryPolicyEnforcement</a>



<a href="https://msdn.microsoft.com/2799e869-e9dd-41de-b808-8e4c52ee9ecf">DhcpV4RemovePolicyRange</a>



<a href="https://msdn.microsoft.com/1e51aea4-f56f-4a7c-95eb-e955e7d173ca">DhcpV4SetPolicy</a>



<a href="https://msdn.microsoft.com/1e87942a-3ee1-442a-a56a-8e63b3003d3b">DhcpV4SetPolicyEnforcement</a>
 

 

