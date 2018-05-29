---
UID: NF:dhcpsapi.DhcpV6GetStatelessStoreParams
title: DhcpV6GetStatelessStoreParams function
author: windows-sdk-content
description: Retrieves the current DHCPv6 stateless client inventory configuration settings at the server or scope level.
old-location: dhcp\dhcpv6getstatelessstoreparams.htm
old-project: DHCP
ms.assetid: 80a32132-a032-452f-9438-52a1eb280fdf
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DhcpV6GetStatelessStoreParams, DhcpV6GetStatelessStoreParams function [DHCP], dhcp.dhcpv6getstatelessstoreparams, dhcpsapi/DhcpV6GetStatelessStoreParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpV6GetStatelessStoreParams
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpV6GetStatelessStoreParams function


## -description


The <b>DhcpV6GetStatelessStoreParams</b> function retrieves the current DHCPv6 stateless client inventory configuration settings at the server or scope level.


## -parameters




### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.


### -param fServerLevel [in]

If <b>TRUE</b> the stateless client inventory configuration settings at server level are retrieved. Otherwise, the scope level configuration settings are retrieved.


### -param SubnetAddress [in]

A <a href="https://msdn.microsoft.com/9623e866-81e5-4d5a-8801-33f0f8973ed3">DHCP_IPV6_ADDRESS</a> structure that contains the IPv6 subnet address of the stateless client inventory configuration settings to be retrieved. 
If the value of <i>fServerLevel</i> is <b>TRUE</b>, this must be 0.


### -param Params [out]

Pointer to a <a href="https://msdn.microsoft.com/852249b2-ea0d-4f83-a41f-12ef8cb029e7">DHCPV6_STATELESS_PARAMS</a> structure that contains the stateless client inventory configuration settings for a DHCPv6 server.


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
IPv6 subnet does not exist on the DHCPv6 server.

</td>
</tr>
</table>
 




## -remarks



<i>Params</i> should be free using <a href="https://msdn.microsoft.com/bf22a0a6-2ecd-4460-89c4-3f870c6275dc">DhcpRpcFreeMemory</a>.




## -see-also




<a href="https://msdn.microsoft.com/4f6ba79c-5ab5-4d89-907d-83bdddbd09a2">DhcpV6GetStatelessStatistics</a>



<a href="https://msdn.microsoft.com/8f64c1bb-8f02-45e3-b9ed-8fce2bf9885c">DhcpV6SetStatelessStoreParams</a>
 

 

