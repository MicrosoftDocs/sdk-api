---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DhcpDeleteClassV6 function


## -description



      The <b>DhcpDeleteClassV6</b> function deletes a DHCP class from the DHCPv6 server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that contains the IPv6 address of the DHCPv6 server. This string is used as a handle for resolving RPC API calls.


### -param ReservedMustBeZero [in]

Reserved. This parameter must be set to 0.


### -param ClassName [in]

Unicode string that specifies the name of the DHCPv6 class to delete.


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
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The class name could not be found in the database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_DELETE_BUILTIN_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The class is a built-in class and cannot be deleted.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5ab20ec9-c809-4d89-8fe6-a5a966e5bff2">DhcpCreateClassV6</a>
 

 

