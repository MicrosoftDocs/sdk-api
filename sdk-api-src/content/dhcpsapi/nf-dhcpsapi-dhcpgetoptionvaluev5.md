---
UID: NF:dhcpsapi.DhcpGetOptionValueV5
title: DhcpGetOptionValueV5 function
author: windows-sdk-content
description: The DhcpGetOptionValueV5 function retrieves a DHCP option value (the option code and associated data) for a particular scope.
old-location: dhcp\dhcpgetoptionvaluev5.htm
old-project: DHCP
ms.assetid: afb598fd-b63f-4dd3-bd6e-287016c5fe57
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpGetOptionValueV5, DhcpGetOptionValueV5 function [DHCP], dhcp.dhcpgetoptionvaluev5, dhcpsapi/DhcpGetOptionValueV5
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - DhcpGetOptionValueV5
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpGetOptionValueV5 function


## -description



      The <b>DhcpGetOptionValueV5</b> function retrieves a DHCP option value (the option code and associated data) for a particular scope. This function extends the functionality provided by <a href="https://msdn.microsoft.com/7dca800f-2427-44b1-bc92-f9db54de08a5">DhcpGetOptionValue</a> by allowing the caller to specify a class and/or vendor for the option.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param Flags [in]

Flag value that indicates whether the option is for a specific or default vendor class.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The option value is retrieved for a default vendor class.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The option value is retrieved for a specific vendor class. The vendor name is supplied in <i>VendorName</i>.

</td>
</tr>
</table>
 


### -param OptionID [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that specifies the code for the option value to retrieve.


### -param ClassName [in]

Unicode string that specifies the DHCP  class name of the option. This parameter is optional.


### -param VendorName [in]

Unicode string that specifies the vendor of the option. This parameter is optional, and should be null when <i>Flags</i> is not set to DHCP_FLAGS_OPTION_IS_VENDOR. If the vendor class is not specified, the option value is returned for the default vendor class.


### -param ScopeInfo [in]


<a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a> structure that contains information on the scope where the option value is set.


### -param OptionValue [out]


<a href="https://msdn.microsoft.com/6a11cb60-2690-45d4-a5e6-a3ebdc1efe3d">DHCP_OPTION_VALUE</a> structure that contains the returned option code and data.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client who is not a member of the "DHCP Administrators" security group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server's database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet is not defined on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition does not exist in the DHCP server database.

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
 




## -see-also




<a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a>



<a href="https://msdn.microsoft.com/6a11cb60-2690-45d4-a5e6-a3ebdc1efe3d">
        DHCP_OPTION_VALUE</a>



<a href="https://msdn.microsoft.com/7dca800f-2427-44b1-bc92-f9db54de08a5">DhcpGetOptionValue</a>



<a href="https://msdn.microsoft.com/05e7930f-e5c1-42e7-a693-f9852cda9494">DhcpSetOptionValueV5</a>
 

 

