---
UID: NF:dhcpsapi.DhcpModifyClass
title: DhcpModifyClass function
author: windows-sdk-content
description: Modifies a DHCP class defined on the server.
old-location: dhcp\dhcpmodifyclass.htm
tech.root: DHCP
ms.assetid: 4ee8897f-d49a-4b60-a26e-e7e11c088353
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpModifyClass, DhcpModifyClass function [DHCP], dhcp.dhcpmodifyclass, dhcpsapi/DhcpModifyClass
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
 - DhcpModifyClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpModifyClass function


## -description


The <b>DhcpModifyClass</b> function modifies a DHCP class defined on the server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ReservedMustBeZero [in]

Reserved. This value must be set to 0.


### -param ClassInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/62fb9f21-ad21-4525-90f4-48dc5a8b230b">DHCP_CLASS_INFO</a> structure that contains the new information for the class.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/62fb9f21-ad21-4525-90f4-48dc5a8b230b">DHCP_CLASS_INFO</a> structure provided in <i>ClassInfo</i> has null or invalid values for the <b>ClassName</b> or <b>ClassData</b> member (or both).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A class name could not be found that matches the provided information.

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
<dt><b>ERROR_DHCP_CLASS_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The new class name is currently in use, or the new class information is currently in use.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/62fb9f21-ad21-4525-90f4-48dc5a8b230b">DHCP_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/ae30baba-a2cd-4662-a62a-58b59d119dc4">DhcpCreateClass</a>



<a href="https://msdn.microsoft.com/45659805-d0d0-4b84-ac98-4a0f53133b0c">DhcpDeleteClass</a>
 

 

