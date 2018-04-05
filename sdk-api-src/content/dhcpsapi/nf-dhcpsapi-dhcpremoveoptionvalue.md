---
UID: NF:dhcpsapi.DhcpRemoveOptionValue
title: DhcpRemoveOptionValue function
author: windows-driver-content
description: Removes the option value for a specific option on the DHCP4 server for the default user class and vendor class, for the specified scope.
old-location: dhcp\dhcpremoveoptionvalue.htm
old-project: DHCP
ms.assetid: e370760c-d392-4e2e-a95c-7213ce593f77
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: DhcpRemoveOptionValue, DhcpRemoveOptionValue function [DHCP], dhcp.dhcpremoveoptionvalue, dhcpsapi/DhcpRemoveOptionValue
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpRemoveOptionValue
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpRemoveOptionValue function


## -description


The <b>DhcpRemoveOptionValue</b> function removes the option value for a specific option on the DHCP4 server for the default user class and vendor class, for the specified scope.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param OptionID [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that contains the code uniquely identifying the specific option to remove from the DHCP server.


### -param ScopeInfo [in]


<a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a> structure that contains information describing the specific scope (default, server, scope, or IPv4 reservation level) from which to remove the option value.


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



<a href="https://msdn.microsoft.com/53b57879-7533-4e92-a179-d6786052ad46">DhcpRemoveOptionValueV5</a>



<a href="https://msdn.microsoft.com/0bcd8c1e-e2ae-46ae-b5ee-6e3373125e71">DhcpSetOptionValue</a>
 

 

