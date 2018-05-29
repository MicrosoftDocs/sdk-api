---
UID: NF:dhcpsapi.DhcpV4GetOptionValue
title: DhcpV4GetOptionValue function
author: windows-sdk-content
description: Retrieves a DHCP option value (the option code and associated data) for a particular scope. This function extends the functionality provided by DhcpGetOptionValueV5 by allowing the caller to specify a policy for the option.
old-location: dhcp\dhcpv4getoptionvalue.htm
old-project: DHCP
ms.assetid: eadb26ec-50d5-474f-b6fe-1a586889bd23
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpV4GetOptionValue, DhcpV4GetOptionValue function [DHCP], dhcp.dhcpv4getoptionvalue, dhcpsapi/DhcpV4GetOptionValue
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
-	DhcpV4GetOptionValue
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpV4GetOptionValue function


## -description


The <b>DhcpV4GetOptionValue</b> function retrieves a DHCP option value (the option code and associated data) for a particular scope. This function extends the functionality provided by <a href="https://msdn.microsoft.com/afb598fd-b63f-4dd3-bd6e-287016c5fe57">DhcpGetOptionValueV5</a> by allowing the caller to specify a policy for the option.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param Flags [in]

Indicates whether the option is for a specific or default vendor.

<table>
<tr>
<th>Flags</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The option value is retrieved for a default vendor.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The option value is retrieved for a specific vendor. The vendor is in <i>VendorName</i>.

</td>
</tr>
</table>
 


### -param OptionID [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> structure that specifies the unique option code for the option value to retrieve. A complete list of standard DHCP and BOOTP option codes can be found at <a href="http://www.ietf.org/rfc/rfc2132.txt">http://www.ietf.org/rfc/rfc2132.txt</a>


### -param PolicyName [in, optional]

A null-terminated Unicode string that represents the name of the policy inside the subnet of the option value to retrieve. The subnet is identified by the <b>SubnetScopeInfo</b> member of <i>ScopeInfo</i>.


### -param VendorName [in, optional]

A null-terminated Unicode string that represents the vendor  of the option. This parameter is optional, and should be <b>NULL</b> when <i>Flags</i> is not <b>DHCP_FLAGS_OPTION_IS_VENDOR</b>. If the vendor is not specified, the option value is returned for the default vendor.


### -param ScopeInfo [in]


<a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a> structure that contains information on the scope of the option value to retrieve.


### -param OptionValue [out]

Pointer to a <a href="https://msdn.microsoft.com/6b2e5866-f65f-4ff0-a531-3d07b972f55e">DHCP_OPTION_DATA</a> structure that contains the data value corresponding to the DHCP option code specified by <i>OptionID</i>.


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
</table>
 




## -remarks



<i>OptionValue</i> should be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.




## -see-also




<a href="https://msdn.microsoft.com/3c2fff2f-3d79-4e0d-8a31-9917088b1413">DhcpV4GetAllOptionValues</a>



<a href="https://msdn.microsoft.com/9f22e44e-0eb8-48a9-8a82-dccf41535ef6">DhcpV4RemoveOptionValue</a>



<a href="https://msdn.microsoft.com/cf8141cc-8cf3-4932-b13a-e276dcdeb825">DhcpV4SetOptionValue</a>



<a href="https://msdn.microsoft.com/8c50af53-8298-401e-826e-0fb1d1410499">DhcpV4SetOptionValues</a>
 

 

