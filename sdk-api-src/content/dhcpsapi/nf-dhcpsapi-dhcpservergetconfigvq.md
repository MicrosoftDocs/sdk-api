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

# DhcpServerGetConfigVQ function


## -description


The <b>DhcpServerGetConfigVQ</b> function retrieves the current DHCP server configuration settings.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ConfigInfo [out]

Pointer to the address of a <a href="https://msdn.microsoft.com/54b5898f-8e9d-42be-b68e-32884d3dbe08">DHCP_SERVER_CONFIG_INFO_VQ</a> structure that contains the returned DHCP server configuration settings.


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
</table>
 




## -remarks



The caller of this function must free the memory pointed to by <i>ConfigInfo</i> by calling <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.




## -see-also




<a href="https://msdn.microsoft.com/54b5898f-8e9d-42be-b68e-32884d3dbe08">DHCP_SERVER_CONFIG_INFO_VQ</a>



<a href="https://msdn.microsoft.com/3498b674-5771-47b6-9dfa-a8e3e10bca40">DhcpServerSetConfigVQ</a>
 

 

