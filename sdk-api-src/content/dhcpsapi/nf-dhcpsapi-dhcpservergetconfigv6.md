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

# DhcpServerGetConfigV6 function


## -description


The <b>DhcpServerGetConfigV6</b> function retrieves the configuration information for the DHCPv6 server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ScopeInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/d5c0cff9-7164-4f14-a0a9-58311390ebd9">DHCP_OPTION_SCOPE_INFO6</a> structure used to identify the DHCPv6 scope for which configuration information will be retrieved.


### -param ConfigInfo [out]

Pointer to the address of a  <a href="https://msdn.microsoft.com/9862f0c1-3c42-4ad7-af3c-15868e4a9314">DHCP_SERVER_CONFIG_INFO_V6</a> structure that contains the requested configuration information.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d5c0cff9-7164-4f14-a0a9-58311390ebd9">DHCP_OPTION_SCOPE_INFO6</a>



<a href="https://msdn.microsoft.com/9862f0c1-3c42-4ad7-af3c-15868e4a9314">DHCP_SERVER_CONFIG_INFO_V6</a>
 

 

