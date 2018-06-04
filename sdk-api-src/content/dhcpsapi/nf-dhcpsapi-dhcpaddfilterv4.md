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

# DhcpAddFilterV4 function


## -description


The <b>DhcpAddFilterV4</b> function adds a link-layer address or address pattern to the allow/deny lists.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param AddFilterInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/eed7fffa-a48c-4ebc-ba3a-a118d2b0e20b">DHCP_FILTER_ADD_INFO</a> structure that contains a link-layer address or address pattern to add to the DHCP server's allow/deny list.


### -param ForceFlag [in]

If <b>TRUE</b>, any existing matching filter is overwritten; if <b>FALSE</b>, the call fails with <b>ERROR_DHCP_LINKLAYER_ADDRESS_EXISTS</b>.


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
<dt><b>ERROR_DHCP_LINKLAYER_ADDRESS_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The address or address pattern already exists in an allow/deny list.

</td>
</tr>
</table>
 




## -remarks



This API allows DHCP clients whose addresses have been added to the allow list to obtain leases, and blocks those added to the deny list. The respective lists must be enabled with a call to <a href="https://msdn.microsoft.com/4a67ad11-1f24-4ab6-b5f7-e51c97562037">DhcpSetFilterV4</a>.




## -see-also




<a href="https://msdn.microsoft.com/eed7fffa-a48c-4ebc-ba3a-a118d2b0e20b">DHCP_FILTER_ADD_INFO</a>



<a href="https://msdn.microsoft.com/4a67ad11-1f24-4ab6-b5f7-e51c97562037">DhcpSetFilterV4</a>
 

 

