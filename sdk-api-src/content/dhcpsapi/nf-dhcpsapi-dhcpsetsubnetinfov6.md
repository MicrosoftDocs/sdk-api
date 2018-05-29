---
UID: NF:dhcpsapi.DhcpSetSubnetInfoV6
title: DhcpSetSubnetInfoV6 function
author: windows-sdk-content
description: Sets or updates the information for an IPv6 subnet defined on the DHCPv6 server.
old-location: dhcp\dhcpsetsubnetinfov6.htm
old-project: DHCP
ms.assetid: 6913881d-a7d5-4465-aadc-5a4dab1a28da
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DhcpSetSubnetInfoV6, DhcpSetSubnetInfoV6 function [DHCP], dhcp.dhcpsetsubnetinfov6, dhcpsapi/DhcpSetSubnetInfoV6
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpSetSubnetInfoV6
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpSetSubnetInfoV6 function


## -description


The <b>DhcpSetSubnetInfoV6</b> function sets or updates the information for an IPv6 subnet defined on the DHCPv6 server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that contains the IPv6 address of the subnet for which the information will be modified.


### -param SubnetInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/cd60f9d0-3ac3-4661-aefe-ddb9052db3e1">DHCP_SUBNET_INFO_V6</a> structure that contains the new or updated information for the IPv6 subnet identified by <i>SubnetAddress</i>.


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
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified subnet is not defined on the DHCP server.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cd60f9d0-3ac3-4661-aefe-ddb9052db3e1">DHCP_SUBNET_INFO_V6</a>
 

 

