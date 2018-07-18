---
UID: NF:dhcpsapi.DhcpSetSuperScopeV4
title: DhcpSetSuperScopeV4 function
author: windows-sdk-content
description: Sets a subnet as the superscope on a DHCP server.
old-location: dhcp\dhcpsetsuperscopev4.htm
old-project: dhcp
ms.assetid: 70da0113-0c4a-4c4e-80ae-1e55773f9904
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: DhcpSetSuperScopeV4, DhcpSetSuperScopeV4 function [DHCP], dhcp.dhcpsetsuperscopev4, dhcpsapi/DhcpSetSuperScopeV4
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
 - DhcpSetSuperScopeV4
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpSetSuperScopeV4 function


## -description


The <b>DhcpSetSuperScopeV4</b> function sets a subnet as the superscope on a DHCP server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that contains the IP address of the subnet that will be defined as the superscope.


### -param SuperScopeName [in, optional]

Pointer to a Unicode string that specifies the new name of the superscope.


### -param ChangeExisting [in]

Specifies whether or not to change an existing superscope to the supplied subnet. If this parameter is <b>TRUE</b> and another subnet is set as the superscope, change the superscope to the supplied subnet; otherwise, if set to <b>FALSE</b> and  another subnet is defined as the superscope, do not change it.


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
 




## -remarks



A <i>superscope</i> is a subnet that contains the complete scope of all addresses available for lease (or are already leased) across the subnet scopes defined on the DHCP server.




## -see-also




<a href="https://msdn.microsoft.com/5d61f39d-8423-43c4-89ab-4c28214ee84d">DhcpDeleteSuperScopeV4</a>
 

 

