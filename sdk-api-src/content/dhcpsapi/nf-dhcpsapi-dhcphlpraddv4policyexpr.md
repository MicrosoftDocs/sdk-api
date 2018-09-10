---
UID: NF:dhcpsapi.DhcpHlprAddV4PolicyExpr
title: DhcpHlprAddV4PolicyExpr function
author: windows-sdk-content
description: Allocates, initializes, and adds a DHCP server policy expression to a DHCP server policy.
old-location: dhcp\dhcphlpraddv4policyexpr.htm
tech.root: dhcp
ms.assetid: 549d86ed-81c1-4126-9f43-f7e5340990d3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpHlprAddV4PolicyExpr, DhcpHlprAddV4PolicyExpr function [DHCP], dhcp.dhcphlpraddv4policyexpr, dhcpsapi/DhcpHlprAddV4PolicyExpr
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
 - DhcpHlprAddV4PolicyExpr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpHlprAddV4PolicyExpr function


## -description


The <b>DhcpHlprAddV4PolicyExpr</b> function allocates, initializes, and adds a DHCP server policy expression to a DHCP server policy.


## -parameters




### -param Policy [in, out]

Pointer to a <a href="https://msdn.microsoft.com/7e62d2f3-275a-45ab-baab-648fe135d0fc">DHCP_POLICY</a> structure that contains the policy to modify


### -param ParentExpr [in]

Integer that specifies the expression index that corresponds to this constituent condition.


### -param Operator [in]

A <a href="https://msdn.microsoft.com/e8faffdc-2fd4-4d7a-ae9f-fd93932b8c10">DHCP_POL_LOGIC_OPER</a> enumeration that defines how the expression is to be evaluated in terms of the results of its constituents.


### -param ExprIndex [out]

Pointer to a <b>DWORD</b> that contains the newly created expression's index in the DHCP server policy.


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
One or more of the  parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_POLICY_BAD_PARENT_EXPR</b></dt>
</dl>
</td>
<td width="60%">
The parent expression specified does not exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7c90625c-e6b5-475f-a9ea-0dfd27810f03">DhcpHlprAddV4PolicyCondition</a>



<a href="https://msdn.microsoft.com/4e5b5fca-7583-43a8-8816-c1003d936233">DhcpHlprAddV4PolicyRange</a>



<a href="https://msdn.microsoft.com/91f04578-9f15-44b4-8cf6-99be13d0395e">DhcpHlprCreateV4Policy</a>



<a href="https://msdn.microsoft.com/ace10974-784b-41f7-aee9-461c8d63b479">DhcpHlprFreeV4Policy</a>



<a href="https://msdn.microsoft.com/46c20727-0e7a-42cf-a571-c1198b124ed0">DhcpHlprIsV4PolicySingleUC</a>



<a href="https://msdn.microsoft.com/f11386a6-2b80-4a2b-b859-fb399d7392e8">DhcpHlprIsV4PolicyValid</a>



<a href="https://msdn.microsoft.com/820b45f6-aa09-4e15-bf77-caa2723f4ea8">DhcpHlprIsV4PolicyWellFormed</a>



<a href="https://msdn.microsoft.com/5d6818f9-4e44-4f24-a489-84defd1117c0">DhcpHlprModifyV4PolicyExpr</a>



<a href="https://msdn.microsoft.com/5f252840-d474-405e-8b32-50e6efe35f62">DhcpHlprResetV4PolicyExpr</a>
 

 

