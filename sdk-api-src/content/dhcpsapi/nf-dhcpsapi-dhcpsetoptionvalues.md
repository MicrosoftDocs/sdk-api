---
UID: NF:dhcpsapi.DhcpSetOptionValues
title: DhcpSetOptionValues function
author: windows-sdk-content
description: Sets option codes and their associated data values for a specific scope defined on the DHCP server.
old-location: dhcp\dhcpsetoptionvalues.htm
old-project: dhcp
ms.assetid: 10a5513d-dfa2-416c-843e-422154db82ee
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpSetOptionValues, DhcpSetOptionValues function [DHCP], dhcp.dhcpsetoptionvalues, dhcpsapi/DhcpSetOptionValues
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.redist: 
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
 - DhcpSetOptionValues
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpSetOptionValues function


## -description


The <b>DhcpSetOptionValues</b> function sets option codes and their associated data values for a specific scope defined on the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ScopeInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a> structure that contains information describing the level (default, server, scope, or IPv4 reservation) at which this option value will be set.


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
The specified DHCP client is not a reserved client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The multicast scope specified in <i>ScopeInfo</i> was not found on the DHCP server.

</td>
</tr>
</table>
 




## -remarks



When this function is called for the first time, it creates the supplied option values in the DHCP server database. Otherwise, it modifies the option values for one or more options   associated with the default user class and vendor class. These values can be set for the default, server, scope, or IPv4 reservation level on the DHCP server.




## -see-also




<a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a>



<a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">DHCP_OPTION_VALUE_ARRAY</a>



<a href="https://msdn.microsoft.com/0bcd8c1e-e2ae-46ae-b5ee-6e3373125e71">DhcpSetOptionValue</a>



<a href="https://msdn.microsoft.com/53549094-d642-4635-9dd6-5ce16d6be08a">DhcpSetOptionValuesV5</a>
 

 

