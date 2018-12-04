---
UID: NF:dhcpsapi.DhcpDeleteSubnetV6
title: DhcpDeleteSubnetV6 function
author: windows-sdk-content
description: The DhcpDeleteSubnetV6 function deletes a subnet from the DHCP server.
old-location: dhcp\dhcpdeletesubnetv6.htm
tech.root: DHCP
ms.assetid: f2c10d8c-ab5f-4a61-89aa-20f2db89db36
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpDeleteSubnetV6, DhcpDeleteSubnetV6 function [DHCP], dhcp.dhcpdeletesubnetv6, dhcpsapi/DhcpDeleteSubnetV6
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - DhcpDeleteSubnetV6
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpDeleteSubnetV6 function


## -description


The <b>DhcpDeleteSubnetV6</b> function deletes a subnet from the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]

DHCP_IPV6_ADDRESS value that contains the IP address of the subnet gateway used to identify the subnet.


### -param ForceFlag [in]


<a href="https://msdn.microsoft.com/2ec45a99-432d-4218-9048-81714ceff36b">DHCP_FORCE_FLAG</a> enumeration value that indicates the type of delete operation to perform (full force or no force).


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified scope element does not exist.

</td>
</tr>
</table>
 



