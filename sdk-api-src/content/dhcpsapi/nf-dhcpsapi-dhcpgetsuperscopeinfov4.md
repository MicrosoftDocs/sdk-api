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

# DhcpGetSuperScopeInfoV4 function


## -description


The <b>DhcpGetSuperScopeInfoV4</b> function returns information on the superscope of a DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param SuperScopeTable [out]


<a href="https://msdn.microsoft.com/ed7ad090-b13a-464b-af03-04944f018b36">DHCP_SUPER_SCOPE_TABLE</a> structure that contains the returned information for the superscope of the supplied DHCP server.

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
</table>
 




## -remarks



A superscope is the set of all subnets defined on a DHCP server, and hence all scopes along with the IP address ranges each serves. Taken altogether, a superscope provides a complete set of all IP addresses served by the DHCP server. The superscope table provides the IP addresses associated with each subnet. To obtain the IP ranges served by each, <a href="https://msdn.microsoft.com/0e511993-a9c3-445b-bafc-3d66182ee32d">DhcpGetSubnetInfo</a> should be called on the IP address provided in each <a href="https://msdn.microsoft.com/affaa0b0-3bd1-4d17-adec-518d2cb7e5b6">DHCP_SUPER_SCOPE_TABLE_ENTRY</a>
        structure of the table.




## -see-also




<a href="https://msdn.microsoft.com/ed7ad090-b13a-464b-af03-04944f018b36">
        DHCP_SUPER_SCOPE_TABLE</a>



<a href="https://msdn.microsoft.com/0e511993-a9c3-445b-bafc-3d66182ee32d">DhcpGetSubnetInfo</a>



<a href="https://msdn.microsoft.com/70da0113-0c4a-4c4e-80ae-1e55773f9904">DhcpSetSuperScopeV4</a>
 

 

