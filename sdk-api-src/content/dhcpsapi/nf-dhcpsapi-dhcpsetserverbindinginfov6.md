---
UID: NF:dhcpsapi.DhcpSetServerBindingInfoV6
title: DhcpSetServerBindingInfoV6 function
author: windows-sdk-content
description: Sets or modifies the IPv6 interface bindings for the DHCPv6 server.
old-location: dhcp\dhcpsetserverbindinginfov6.htm
old-project: dhcp
ms.assetid: 55eb2073-87c4-49b1-b294-35bfeb13d530
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpSetServerBindingInfoV6, DhcpSetServerBindingInfoV6 function [DHCP], dhcp.dhcpsetserverbindinginfov6, dhcpsapi/DhcpSetServerBindingInfoV6
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
 - DhcpSetServerBindingInfoV6
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpSetServerBindingInfoV6 function


## -description


The <b>DhcpSetServerBindingInfoV6</b> function sets or modifies the IPv6 interface bindings for the DHCPv6 server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param Flags [in]

This parameter is not used and must be set to 0.


### -param BindElementInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/b78ebdf8-da24-418c-8fe8-aed3047dfdf3">DHCPV6_BIND_ELEMENT_ARRAY</a> structure that contains the IPv6 interface bindings for the DHCPv6 server.


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
<dt><b>ERROR_DHCP_NETWORK_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
The network has changed. Retry this operation after checking for network changes. Network changes can be caused by interfaces that are either new or no longer valid, or by IPv6 addresses that are either new or no longer valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CANNOT_MODIFY_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The supplied bindings to internal IPv6 addresses cannot be modified. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b78ebdf8-da24-418c-8fe8-aed3047dfdf3">DHCPV6_BIND_ELEMENT_ARRAY</a>



<a href="https://msdn.microsoft.com/1f33ac24-d547-4913-bc37-51627bb3af6a">DhcpGetServerBindingInfoV6</a>
 

 

