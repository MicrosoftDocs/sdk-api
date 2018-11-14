---
UID: NF:dhcpsapi.DhcpV4QueryPolicyEnforcement
title: DhcpV4QueryPolicyEnforcement function
author: windows-sdk-content
description: Retrieves the policy enforcement state on the server or the specified IPv4 subnet from the DHCP Server.
old-location: dhcp\dhcpv4querypolicyenforcement.htm
tech.root: DHCP
ms.assetid: a622d83c-bb18-4482-be8d-fdd96382a5e1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpV4QueryPolicyEnforcement, DhcpV4QueryPolicyEnforcement function [DHCP], dhcp.dhcpv4querypolicyenforcement, dhcpsapi/DhcpV4QueryPolicyEnforcement
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
 - DhcpV4QueryPolicyEnforcement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DhcpV4QueryPolicyEnforcement
: 
---

# DhcpV4QueryPolicyEnforcement function


## -description


The <b>DhcpV4QueryPolicyEnforcement</b> function  retrieves the policy enforcement state on the server or the specified IPv4 subnet from the DHCP Server.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param fGlobalPolicy [in]

If <b>TRUE</b> the policy enforcement state of the server is retrieved. Otherwise, the policy enforcement state of specified Ipv4 scope is retrieved.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that contains the IPv4 subnet address of the policy enforcement state to retrieve.


### -param Enabled [out]

Pointer to a <b>BOOL</b> that indicates the state of policy enforcement. If  <b>TRUE</b> the policy enforcement state is enabled. Otherwise, the policy enforcement state is disabled.

<div class="alert"><b>Note</b>  The memory for this must be allocated by the caller.

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
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet does not exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/43ec0634-6a4b-4d70-98d1-410b33a7cb17">DhcpV4AddPolicyRange</a>



<a href="https://msdn.microsoft.com/c42e9c64-d028-4489-82dc-85ce9a6d6c09">DhcpV4CreatePolicy</a>



<a href="https://msdn.microsoft.com/94e6ad23-3e38-4ee2-bc3a-8d7ff1b21eca">DhcpV4DeletePolicy</a>



<a href="https://msdn.microsoft.com/c3915699-f60d-495c-81df-85dc6fe2657c">DhcpV4EnumPolicies</a>



<a href="https://msdn.microsoft.com/a6112bf8-5c1f-4f33-ba1f-b4903cc6befa">DhcpV4GetPolicy</a>



<a href="https://msdn.microsoft.com/2799e869-e9dd-41de-b808-8e4c52ee9ecf">DhcpV4RemovePolicyRange</a>



<a href="https://msdn.microsoft.com/1e51aea4-f56f-4a7c-95eb-e955e7d173ca">DhcpV4SetPolicy</a>



<a href="https://msdn.microsoft.com/1e87942a-3ee1-442a-a56a-8e63b3003d3b">DhcpV4SetPolicyEnforcement</a>
 

 

