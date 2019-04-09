---
UID: NF:dhcpsapi.DhcpEnumOptionValues
title: DhcpEnumOptionValues function (dhcpsapi.h)
author: windows-sdk-content
description: Returns an enumerated list of option values (just the option data and the associated ID number) for a given scope.
old-location: dhcp\dhcpenumoptionvalues.htm
tech.root: DHCP
ms.assetid: 4054cab9-b5f9-4ffa-8151-3ea705bc0755
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DhcpEnumOptionValues, DhcpEnumOptionValues function [DHCP], dhcp.dhcpenumoptionvalues, dhcpsapi/DhcpEnumOptionValues
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
 - DhcpEnumOptionValues
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpEnumOptionValues function


## -description


The <b>DhcpEnumOptionValues</b> function returns an enumerated list of option values (just the option data and the associated ID number) for a given scope.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ScopeInfo [in]


<a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a> structure that contains the  level (specifically: default, server, scope, or IPv4 reservation level) for which the option values are defined and should be enumerated. 


### -param ResumeHandle [in, out]

Pointer to a <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes worth of option values  are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth.

The presence of additional enumerable data is indicated when this function returns ERROR_MORE_DATA. If no additional enumerable data is available on the DHCPv4 server, ERROR_NO_MORE_ITEMS is returned.


### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of option values to return. If the number of remaining unenumerated options (in bytes) is less than this value, then that amount will be returned.

To retrieve all the option values for the default user and vendor class at the specified level, set this parameter to 0xFFFFFFFF.


### -param OptionValues [out]

Pointer to a <a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">DHCP_OPTION_VALUE_ARRAY</a> structure that contains the enumerated option values returned for the specified scope. If there are no option values available for this scope on the DHCP server, this parameter will return null.


### -param OptionsRead [out]

Pointer to a DWORD value that specifies the number of option values returned in <i>OptionValues</i>.


### -param OptionsTotal [out]

Pointer to a DWORD value that specifies the total number of remaining option values for this scope stored on the DHCP server.


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
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server database.

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet does not exist on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_NOT_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCPv4 client is not an IPv4 reserved client.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">DHCP_OPTION_VALUE_ARRAY</a>



<a href="https://msdn.microsoft.com/4c63161d-7d61-402c-8a5e-2800bdc5e18f">DhcpEnumOptionValuesV5</a>
 

 

