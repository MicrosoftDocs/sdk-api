---
UID: NF:dhcpsapi.DhcpV4DeletePolicy
title: DhcpV4DeletePolicy function
author: windows-driver-content
description: Deletes an existing policy from the DHCP Server.
old-location: dhcp\dhcpv4deletepolicy.htm
old-project: DHCP
ms.assetid: 94e6ad23-3e38-4ee2-bc3a-8d7ff1b21eca
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: DhcpV4DeletePolicy, DhcpV4DeletePolicy function [DHCP], dhcp.dhcpv4deletepolicy, dhcpsapi/DhcpV4DeletePolicy
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	DhcpV4DeletePolicy
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpV4DeletePolicy function


## -description


The <b>DhcpV4DeletePolicy</b> function deletes an existing policy from the DHCP Server.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param fGlobalPolicy [in]

If <b>TRUE</b> the server level policy is deleted. Otherwise, the scope level policy is deleted.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that contains the IPv4 subnet address of the policy to delete.


### -param PolicyName [in]

A null-terminated Unicode string that represents the name of the policy to delete.


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
<dt><b>ERROR_DHCP_POLICY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The DHCP server policy was not found.

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



<a href="https://msdn.microsoft.com/c42e9c64-d028-4489-82dc-85ce9a6d6c09">DhcpV4CreatePolicy</a>



<a href="https://msdn.microsoft.com/c3915699-f60d-495c-81df-85dc6fe2657c">DhcpV4EnumPolicies</a>



<a href="https://msdn.microsoft.com/a6112bf8-5c1f-4f33-ba1f-b4903cc6befa">DhcpV4GetPolicy</a>



<a href="https://msdn.microsoft.com/a622d83c-bb18-4482-be8d-fdd96382a5e1">DhcpV4QueryPolicyEnforcement</a>



<a href="https://msdn.microsoft.com/2799e869-e9dd-41de-b808-8e4c52ee9ecf">DhcpV4RemovePolicyRange</a>



<a href="https://msdn.microsoft.com/1e51aea4-f56f-4a7c-95eb-e955e7d173ca">DhcpV4SetPolicy</a>



<a href="https://msdn.microsoft.com/1e87942a-3ee1-442a-a56a-8e63b3003d3b">DhcpV4SetPolicyEnforcement</a>
 

 

