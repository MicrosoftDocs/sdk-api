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

# DhcpV6GetFreeIPAddress function


## -description


The <b>DhcpV6GetFreeIPAddress</b> function  retrieves the list of available IPv6 addresses that can be leased to clients.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param ScopeId [in]


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that specifies the IPv6 subnet ID from which available addresses to lease to clients are retrieved.


### -param StartIP

TBD


### -param EndIP

TBD


### -param NumFreeAddrReq

TBD


### -param IPAddrList [out]

Pointer to a <a href="https://msdn.microsoft.com/B87CF991-FFC8-4CB4-8EE9-66716EC9B58D">DHCPV6_IP_ARRAY</a> structure that contains the list of available IPv6 addresses that can be leased to clients.


#### - endIP [in]


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that specifies the scope IPv6 range's end point address from where the available addresses are retrieved. If this parameter is 0, the end address of the IPv6 subnet specified by <i>ScopeId</i> parameter is taken as the default.


#### - numFreeAddrReq [in]

Integer that specifies the number of IPv6 addresses retrieved from the specified scope in <i>IPAddrList</i>. If this parameter is 0, only one IPv6 address is returned.


#### - startIP [in]


<a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that specifies the scope IPv6 range's starting point address from where the available addresses are retrieved. If this parameter is 0, the start address of the IPv6 subnet specified by <i>ScopeId</i> is the default.


## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
IPv6 subnet does not exist on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_REACHED_END_OF_SELECTION</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP server has reached the end of the selected range while finding the free IP address.

</td>
</tr>
</table>
 




## -remarks



<i>IPAddrList</i> should be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.

The maximum number of IPv6 addresses returned is 1024. To retrieve more that 1024 IPv6 addresses, multiple calls to  <b>DhcpV6GetFreeIPAddress</b> must be made. After the initial call, each subsequent call to <b>DhcpV6GetFreeIPAddress</b> must set <i>startIP</i> to the last address in the list received in <i>IPAddrList</i> from the previous call to <b>DhcpV6GetFreeIPAddress</b>.

When the number of free IPv6 addresses available on the DHCP server is less than that requested, the list of free IPv6 addresses available are returned to the caller with error code <b>ERROR_DHCP_REACHED_END_OF_SELECTION</b>.



