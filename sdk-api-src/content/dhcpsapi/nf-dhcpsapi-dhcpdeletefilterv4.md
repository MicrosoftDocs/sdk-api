---
UID: NF:dhcpsapi.DhcpDeleteFilterV4
title: DhcpDeleteFilterV4 function
author: windows-sdk-content
description: Deletes a link-layer address or address pattern from a DHCP server's allow/deny lists.
old-location: dhcp\dhcpdeletefilterv4.htm
tech.root: DHCP
ms.assetid: ba59bfed-63dd-4468-bc2a-ed47d093c23c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DhcpDeleteFilterV4, DhcpDeleteFilterV4 function [DHCP], dhcp.dhcpdeletefilterv4, dhcpsapi/DhcpDeleteFilterV4
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
 - DhcpDeleteFilterV4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpDeleteFilterV4 function


## -description


The <b>DhcpDeleteFilterV4</b> function deletes a link-layer address or address pattern from a DHCP server's allow/deny lists.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param DeleteFilterInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/8c645b03-9859-48e9-8974-2dbdc9cfcac6">DHCP_ADDR_PATTERN</a> structure that contains the link-layer address or address pattern filter to remove from the DHCP server database.


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
<dt><b>ERROR_DHCP_LINKLAYER_ADDRESS_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The address or address pattern does not exist in an allow/deny list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The address or address pattern supplied in <i>DeleteFilterInfo</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8c645b03-9859-48e9-8974-2dbdc9cfcac6">DHCP_ADDR_PATTERN</a>



<a href="https://msdn.microsoft.com/5543ef67-d095-44b8-b511-e6754aeb9881">DhcpAddFilterV4</a>
 

 

