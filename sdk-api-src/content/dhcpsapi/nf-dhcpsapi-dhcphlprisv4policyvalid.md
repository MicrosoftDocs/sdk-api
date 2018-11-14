---
UID: NF:dhcpsapi.DhcpHlprIsV4PolicyValid
title: DhcpHlprIsV4PolicyValid function
author: windows-sdk-content
description: Verifies a DHCP server policy.
old-location: dhcp\dhcphlprisv4policyvalid.htm
tech.root: DHCP
ms.assetid: f11386a6-2b80-4a2b-b859-fb399d7392e8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpHlprIsV4PolicyValid, DhcpHlprIsV4PolicyValid function [DHCP], dhcp.dhcphlprisv4policyvalid, dhcpsapi/DhcpHlprIsV4PolicyValid
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
 - DhcpHlprIsV4PolicyValid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DhcpHlprIsV4PolicyValid
: 
---

# DhcpHlprIsV4PolicyValid function


## -description


The <b>DhcpHlprIsV4PolicyValid</b> function verifies a DHCP server policy.


## -parameters




### -param pPolicy [in]

Pointer to <a href="https://msdn.microsoft.com/7e62d2f3-275a-45ab-baab-648fe135d0fc">DHCP_POLICY</a> structure that contains the policy to verify.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter was invalid.

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
<dt><b>ERROR_DHCP_POLICY_RANGE_BAD</b></dt>
</dl>
</td>
<td width="60%">
The specified policy range is not contained within the IP address range of the scope or the specified policy range is invalid.

</td>
</tr>
</table>
 




## -remarks



The API performs the following validations on the policy structure.
   

<ol>
<li>The policy must be well formed.</li>
<li>Server policies must not have any ranges.</li>
<li>Server policies must have the subnet address set to 0.0.0.0.</li>
<li>Scope policies must have a subnet address.</li>
<li>All associated ranges must be valid and non-overlapping.</li>
<li>For all expressions, the parent expression index must be set to 0.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/7c90625c-e6b5-475f-a9ea-0dfd27810f03">DhcpHlprAddV4PolicyCondition</a>



<a href="https://msdn.microsoft.com/549d86ed-81c1-4126-9f43-f7e5340990d3">DhcpHlprAddV4PolicyExpr</a>



<a href="https://msdn.microsoft.com/4e5b5fca-7583-43a8-8816-c1003d936233">DhcpHlprAddV4PolicyRange</a>



<a href="https://msdn.microsoft.com/91f04578-9f15-44b4-8cf6-99be13d0395e">DhcpHlprCreateV4Policy</a>



<a href="https://msdn.microsoft.com/ace10974-784b-41f7-aee9-461c8d63b479">DhcpHlprFreeV4Policy</a>



<a href="https://msdn.microsoft.com/46c20727-0e7a-42cf-a571-c1198b124ed0">DhcpHlprIsV4PolicySingleUC</a>



<a href="https://msdn.microsoft.com/820b45f6-aa09-4e15-bf77-caa2723f4ea8">DhcpHlprIsV4PolicyWellFormed</a>



<a href="https://msdn.microsoft.com/5d6818f9-4e44-4f24-a489-84defd1117c0">DhcpHlprModifyV4PolicyExpr</a>



<a href="https://msdn.microsoft.com/5f252840-d474-405e-8b32-50e6efe35f62">DhcpHlprResetV4PolicyExpr</a>
 

 

