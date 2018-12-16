---
UID: NF:dhcpsapi.DhcpGetServerBindingInfoV6
title: DhcpGetServerBindingInfoV6 function
author: windows-sdk-content
description: Retrieves an array of IPv6 interface binding information specific to the DHCPv6 server.
old-location: dhcp\dhcpgetserverbindinginfov6.htm
tech.root: DHCP
ms.assetid: 1f33ac24-d547-4913-bc37-51627bb3af6a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DhcpGetServerBindingInfoV6, DhcpGetServerBindingInfoV6 function [DHCP], dhcp.dhcpgetserverbindinginfov6, dhcpsapi/DhcpGetServerBindingInfoV6
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
 - DhcpGetServerBindingInfoV6
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpGetServerBindingInfoV6 function


## -description


The <b>DhcpGetServerBindingInfoV6</b> function retrieves an array of IPv6 interface binding information specific to the DHCPv6 server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param Flags [in]

This parameter is not used, and must be set to 0.


### -param BindElementsInfo [out]

Pointer to the address of a <a href="https://msdn.microsoft.com/b78ebdf8-da24-418c-8fe8-aed3047dfdf3">DHCPV6_BIND_ELEMENT_ARRAY</a> structure that contains the information about the IPv6 interface bindings for the DHCPv6 server.


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
</table>
 




## -remarks



The caller of this function must free the memory pointed to by <i>BindElementsInfo</i>.




## -see-also




<a href="https://msdn.microsoft.com/b78ebdf8-da24-418c-8fe8-aed3047dfdf3">DHCPV6_BIND_ELEMENT_ARRAY</a>
 

 

