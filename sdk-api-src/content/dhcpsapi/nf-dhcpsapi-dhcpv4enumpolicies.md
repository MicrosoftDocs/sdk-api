---
UID: NF:dhcpsapi.DhcpV4EnumPolicies
title: DhcpV4EnumPolicies function
author: windows-sdk-content
description: Enumerates the policies configured on the DHCP Server.
old-location: dhcp\dhcpv4enumpolicies.htm
old-project: dhcp
ms.assetid: c3915699-f60d-495c-81df-85dc6fe2657c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpV4EnumPolicies, DhcpV4EnumPolicies function [DHCP], dhcp.dhcpv4enumpolicies, dhcpsapi/DhcpV4EnumPolicies
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
tech.root: 
req.typenames: QuarantineStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpV4EnumPolicies
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpV4EnumPolicies function


## -description


The <b>DhcpV4EnumPolicies</b> function enumerates the policies configured on the DHCP Server.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param ResumeHandle [in, out]

Pointer to a  <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_RESUME_HANDLE</a> structure that identifies this enumeration for use in subsequent calls to this function.

Initially, this value should be zero on input. If successful, the returned value should be used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 100, and 200 policies are configured on the server, the resume handle can be used after the first 100 policies are retrieved to obtain the next 100 on a subsequent call.


### -param PreferredMaximum [in]

The maximum number of policy structures to return in <i>EnumInfo</i>. If <i>PreferredMaximum</i> is greater than the number of remaining non-enumerated policies on the server, the remaining number of  non-enumerated policies is returned.


### -param fGlobalPolicy [in]

If <b>TRUE</b> the server level policy is enumerated. Otherwise, the scope level policy is enumerated.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> structure that contains the IPv4 subnet address of the policies to enumerate.


### -param EnumInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/220CD2F8-AFB4-4B87-9B10-904AD04E4C1F">DHCP_POLICY_ARRAY</a> structure that contains the policies available on the DHCP server. If no policies are configured, this value is <b>NULL</b>.


### -param ElementsRead [out]

Pointer to a <b>DWORD</b> that specifies the number of policies returned in <i>EnumInfo</i>.


### -param ElementsTotal [out]

Pointer to a <b>DWORD</b>  that specifies the number of policies configured on the DHCP server that have not yet been enumerated.


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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
There are more elements available to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more elements left to enumerate.

</td>
</tr>
</table>
 




## -remarks



<i>EnumInfo</i> should be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

<i>SubnetAddress</i> must be in host-byte ordering.




## -see-also




<a href="https://msdn.microsoft.com/43ec0634-6a4b-4d70-98d1-410b33a7cb17">DhcpV4AddPolicyRange</a>



<a href="https://msdn.microsoft.com/c42e9c64-d028-4489-82dc-85ce9a6d6c09">DhcpV4CreatePolicy</a>



<a href="https://msdn.microsoft.com/94e6ad23-3e38-4ee2-bc3a-8d7ff1b21eca">DhcpV4DeletePolicy</a>



<a href="https://msdn.microsoft.com/a6112bf8-5c1f-4f33-ba1f-b4903cc6befa">DhcpV4GetPolicy</a>



<a href="https://msdn.microsoft.com/a622d83c-bb18-4482-be8d-fdd96382a5e1">DhcpV4QueryPolicyEnforcement</a>



<a href="https://msdn.microsoft.com/2799e869-e9dd-41de-b808-8e4c52ee9ecf">DhcpV4RemovePolicyRange</a>



<a href="https://msdn.microsoft.com/1e51aea4-f56f-4a7c-95eb-e955e7d173ca">DhcpV4SetPolicy</a>



<a href="https://msdn.microsoft.com/1e87942a-3ee1-442a-a56a-8e63b3003d3b">DhcpV4SetPolicyEnforcement</a>
 

 

