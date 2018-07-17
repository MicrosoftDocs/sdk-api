---
UID: NF:dhcpsapi.DhcpDeleteSuperScopeV4
title: DhcpDeleteSuperScopeV4 function
author: windows-sdk-content
description: Deletes a superscope from the DHCP server.
old-location: dhcp\dhcpdeletesuperscopev4.htm
old-project: DHCP
ms.assetid: 5d61f39d-8423-43c4-89ab-4c28214ee84d
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DhcpDeleteSuperScopeV4, DhcpDeleteSuperScopeV4 function [DHCP], dhcp.dhcpdeletesuperscopev4, dhcpsapi/DhcpDeleteSuperScopeV4
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
 - DhcpDeleteSuperScopeV4
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpDeleteSuperScopeV4 function


## -description


The <b>DhcpDeleteSuperScopeV4</b> function deletes a superscope from the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SuperScopeName [in]

Unicode string that specifies the name of the superscope to delete.


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
The specified IPv4 subnet does not exist on the DHCP server.

</td>
</tr>
</table>
 




## -remarks



Deleting a superscope does not delete the subnets present in the superscope; it simply removes the table that groups the subnets into a superscope. Individual subnets should be deleted using <a href="https://msdn.microsoft.com/e000a81b-b61b-4ba9-adee-4940edc78050">DhcpDeleteSubnet</a>.




## -see-also




<a href="https://msdn.microsoft.com/f40c77b8-c8ad-432d-8a9e-6719630826ef">DhcpGetSuperScopeInfoV4</a>



<a href="https://msdn.microsoft.com/70da0113-0c4a-4c4e-80ae-1e55773f9904">DhcpSetSuperScopeV4</a>
 

 

