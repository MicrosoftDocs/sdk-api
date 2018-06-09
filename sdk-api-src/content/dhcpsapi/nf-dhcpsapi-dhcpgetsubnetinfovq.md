---
UID: NF:dhcpsapi.DhcpGetSubnetInfoVQ
title: DhcpGetSubnetInfoVQ function
author: windows-sdk-content
description: Retrieves the information about a specific IPv4 subnet defined on the DHCP server.
old-location: dhcp\dhcpgetsubnetinfovq.htm
old-project: DHCP
ms.assetid: 7ee3ba38-a90c-4409-a40f-80e1cd1fc3c3
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: DhcpGetSubnetInfoVQ, DhcpGetSubnetInfoVQ function [DHCP], dhcp.dhcpgetsubnetinfovq, dhcpsapi/DhcpGetSubnetInfoVQ
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
 - DhcpGetSubnetInfoVQ
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpGetSubnetInfoVQ function


## -description



      The <b>DhcpGetSubnetInfoVQ</b> function retrieves the information about a specific IPv4 subnet defined on the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]

<b>DHCP_IP_ADDRESS</b> structure that contains the IPv4 address of the subnet for which the information will be modified.


### -param SubnetInfo [out]

A <a href="https://msdn.microsoft.com/8440378e-c1dc-4e22-8c56-2cf4412c2483">DHCP_SUBNET_INFO_VQ</a> structure that contains the returned information for the subnet matching the IPv4 address specified by <i>SubnetAddress</i>.

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
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified subnet is not defined on the DHCP server.

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




<a href="https://msdn.microsoft.com/8440378e-c1dc-4e22-8c56-2cf4412c2483">
        DHCP_SUBNET_INFO_VQ</a>
 

 

