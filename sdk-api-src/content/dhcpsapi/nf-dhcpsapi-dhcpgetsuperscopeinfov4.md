---
UID: NF:dhcpsapi.DhcpGetSuperScopeInfoV4
title: DhcpGetSuperScopeInfoV4 function
author: windows-sdk-content
description: Returns information on the superscope of a DHCP server.
old-location: dhcp\dhcpgetsuperscopeinfov4.htm
old-project: dhcp
ms.assetid: f40c77b8-c8ad-432d-8a9e-6719630826ef
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpGetSuperScopeInfoV4, DhcpGetSuperScopeInfoV4 function [DHCP], dhcp.dhcpgetsuperscopeinfov4, dhcpsapi/DhcpGetSuperScopeInfoV4
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
 - DhcpGetSuperScopeInfoV4
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
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



A superscope is the set of all subnets defined on a DHCP server, and hence all scopes along with the IP address ranges each serves. Taken altogether, a superscope provides a complete set of all IP addresses served by the DHCP server. The superscope table provides the IP addresses associated with each subnet. To obtain the IP ranges served by each, <a href="https://msdn.microsoft.com/0e511993-a9c3-445b-bafc-3d66182ee32d">DhcpGetSubnetInfo</a> should be called on the IP address provided in each <a href="https://msdn.microsoft.com/affaa0b0-3bd1-4d17-adec-518d2cb7e5b6">DHCP_SUPER_SCOPE_TABLE_ENTRY</a>structure of the table.




## -see-also




<a href="https://msdn.microsoft.com/ed7ad090-b13a-464b-af03-04944f018b36">DHCP_SUPER_SCOPE_TABLE</a>



<a href="https://msdn.microsoft.com/0e511993-a9c3-445b-bafc-3d66182ee32d">DhcpGetSubnetInfo</a>



<a href="https://msdn.microsoft.com/70da0113-0c4a-4c4e-80ae-1e55773f9904">DhcpSetSuperScopeV4</a>
 

 

