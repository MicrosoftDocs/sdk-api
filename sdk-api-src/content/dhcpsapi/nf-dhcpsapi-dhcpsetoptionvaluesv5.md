---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DhcpSetOptionValuesV5 function


## -description


The <b>DhcpSetOptionValuesV5</b> function sets option codes and their associated data values for a specific scope defined on the DHCP server. This function extends the functionality provided by <a href="https://msdn.microsoft.com/10a5513d-dfa2-416c-843e-422154db82ee">DhcpSetOptionValues</a> by allowing the caller to specify a class and/or vendor for the options.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IPv4 address of the DHCP server.


### -param Flags [in]

This parameter must be set to 0 and ignored upon receipt.


### -param ClassName [in]

Unicode string that specifies the DHCP  class  of the options. This parameter is optional.


### -param VendorName [in]

Unicode string that specifies the vendor of the options. If no vendor class is specified, then the option value is set for the default vendor class. This parameter is optional.


### -param ScopeInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a> structure that contains information describing the DHCP scope these option values will be set on. This parameter indicates whether the option value is set for the default, server, or scope level, or for an IPv4 reservation.


### -param OptionValues [in]

Pointer to a <a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">DHCP_OPTION_VALUE_ARRAY</a> structure that contains a list of option codes and the corresponding data value that will be set for them.


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
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition could not be found in the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_NOT_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP client is not an IPv4 reserved client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified class name cannot be found in the DHCP server database.

</td>
</tr>
</table>
 




## -remarks



The caller of this function must release the memory pointed to by <i>OptionValues</i> after the call completes.




## -see-also




<a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">
        DHCP_OPTION_SCOPE_INFO</a>



<a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">
        DHCP_OPTION_VALUE_ARRAY</a>



<a href="https://msdn.microsoft.com/53549094-d642-4635-9dd6-5ce16d6be08a">DhcpSetOptionValueV5</a>



<a href="https://msdn.microsoft.com/10a5513d-dfa2-416c-843e-422154db82ee">DhcpSetOptionValues</a>
 

 

