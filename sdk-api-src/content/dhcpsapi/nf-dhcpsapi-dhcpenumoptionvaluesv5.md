---
UID: NF:dhcpsapi.DhcpEnumOptionValuesV5
title: DhcpEnumOptionValuesV5 function (dhcpsapi.h)
author: windows-sdk-content
description: The DhcpEnumOptionValuesV5 function returns an enumerated list of option values (just the option data and the associated ID number) for a specific scope within a given user or vendor class.
old-location: dhcp\dhcpenumoptionvaluesv5.htm
tech.root: DHCP
ms.assetid: 4c63161d-7d61-402c-8a5e-2800bdc5e18f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpEnumOptionValuesV5, DhcpEnumOptionValuesV5 function [DHCP], dhcp.dhcpenumoptionvaluesv5, dhcpsapi/DhcpEnumOptionValuesV5
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
 - DhcpEnumOptionValuesV5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpEnumOptionValuesV5 function


## -description


The <b>DhcpEnumOptionValuesV5</b> function returns an enumerated list of option values (just the option data and the associated ID number) for a specific scope within a given user or vendor class.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param Flags [in]

Specifies a bit flag that indicates whether or not the option is vendor specific. If it is not vendor specific, this parameter must be 0.

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
The option values are enumerated for a default vendor class.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The option values are enumerated for a specific vendor class.

</td>
</tr>
</table>
 


### -param ClassName [in]

Pointer to a Unicode string that contains the name of the class whose scope option values will be enumerated.


### -param VendorName [in]

Pointer to a Unicode string that contains the name of the vendor for the class. This parameter is optional. If a vendor class name is not provided, the option values enumerated for a default vendor class.


### -param ScopeInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a> structure that contains the  scope for which the option values are defined. This value defines the option values that will be retrieved from the server, scope, or default level, or for an IPv4 reservation.


### -param ResumeHandle [in, out]

Pointer to a <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes' worth of option values  are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth.


### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of option values to return. If the number of remaining unenumerated options (in bytes) is less than this value, all option values are returned.


### -param OptionValues [out]

Pointer to a <a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">DHCP_OPTION_VALUE_ARRAY</a> structure that contains the enumerated option values returned for the specified scope. If there are no option values available for this scope on the DHCP server, this parameter will return null.


### -param OptionsRead [out]

Pointer to a DWORD value that specifies the number of option values returned in <i>OptionValues</i>.


### -param OptionsTotal [out]

Pointer to a DWORD value that specifies the total number of as-yet unenumerated option values for this scope stored on the DHCP server.


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
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The supplied user or vendor class name is either incorrect or unknown.

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



<a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">DHCP_OPTION_VALUE_ARRAY</a>
 

 

