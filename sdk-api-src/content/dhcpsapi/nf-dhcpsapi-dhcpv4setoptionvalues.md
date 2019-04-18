---
UID: NF:dhcpsapi.DhcpV4SetOptionValues
title: DhcpV4SetOptionValues function (dhcpsapi.h)
author: windows-sdk-content
description: Sets option codes and their associated data values for a specific scope defined on the DHCP server. This function extends the functionality provided by DhcpSetOptionValuesV5 by allowing the caller to specify a policy for the options.
old-location: dhcp\dhcpv4setoptionvalues.htm
tech.root: DHCP
ms.assetid: 8c50af53-8298-401e-826e-0fb1d1410499
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DhcpV4SetOptionValues, DhcpV4SetOptionValues function [DHCP], dhcp.dhcpv4setoptionvalues, dhcpsapi/DhcpV4SetOptionValues
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
 - DhcpV4SetOptionValues
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DhcpV4SetOptionValues function


## -description


The <b>DhcpV4SetOptionValues</b> function  sets option codes and their associated data values for a specific scope defined on the DHCP server. This function extends the functionality provided by <a href="https://msdn.microsoft.com/53549094-d642-4635-9dd6-5ce16d6be08a">DhcpSetOptionValuesV5</a> by allowing the caller to specify a policy for the options.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param Flags [in]

Reserved. Must be 0.


### -param PolicyName [in, optional]

A null-terminated Unicode string that represents the name of the policy inside the subnet of the option value to set. The subnet is identified by the <b>SubnetScopeInfo</b> member of <i>ScopeInfo</i>.


### -param VendorName [in, optional]

A null-terminated Unicode string that represents the vendor  of the option. This parameter is optional, and if <b>NULL</b>, the option value is set for the default vendor.


### -param ScopeInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a> structure that contains information describing the DHCP scope of the option values to set. This parameter specifies whether the option value is set for the default, server, or scope level, or for an IPv4 reservation.


### -param OptionValues [in]

Pointer to a <a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">DHCP_OPTION_VALUE_ARRAY</a> structure that contains a list of option codes and the corresponding data value that will be set.


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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The class name being used is unknown or incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_POLICY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified policy name does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition does not exist on the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_NOT_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP client is not a reserved client.

</td>
</tr>
</table>
 




## -remarks



<i>OptionValues</i> and its member, <b>Values</b>, should be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.




## -see-also




<a href="https://msdn.microsoft.com/3c2fff2f-3d79-4e0d-8a31-9917088b1413">DhcpV4GetAllOptionValues</a>



<a href="https://msdn.microsoft.com/eadb26ec-50d5-474f-b6fe-1a586889bd23">DhcpV4GetOptionValue</a>



<a href="https://msdn.microsoft.com/9f22e44e-0eb8-48a9-8a82-dccf41535ef6">DhcpV4RemoveOptionValue</a>



<a href="https://msdn.microsoft.com/cf8141cc-8cf3-4932-b13a-e276dcdeb825">DhcpV4SetOptionValue</a>
 

 

