---
UID: NF:dhcpsapi.DhcpGetMibInfoV6
title: DhcpGetMibInfoV6 function (dhcpsapi.h)
author: windows-sdk-content
description: Retrieves the IPv6 counter values of the DHCP server.
old-location: dhcp\dhcpgetmibinfov6.htm
tech.root: DHCP
ms.assetid: fcc61321-2edd-4ea8-bcd7-7237fbc90b74
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DhcpGetMibInfoV6, DhcpGetMibInfoV6 function [DHCP], dhcp.dhcpgetmibinfov6, dhcpsapi/DhcpGetMibInfoV6
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
 - DhcpGetMibInfoV6
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DhcpGetMibInfoV6 function


## -description


The <b>DhcpGetMibInfoV6</b> function retrieves the IPv6 counter values of the DHCP server. 


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCPv6 server.


### -param MibInfo [out]

Pointed to a <a href="https://msdn.microsoft.com/8b961666-4b55-47b4-be52-81b67c9d1cae">DHCP_MIB_INFO_V6</a> structure that points to the location containing the IPv6 MIB information about the DHCP server.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters provides an invalid value.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8b961666-4b55-47b4-be52-81b67c9d1cae">DHCP_MIB_INFO_V6</a>
 

 

