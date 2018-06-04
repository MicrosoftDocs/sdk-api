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
 

 

