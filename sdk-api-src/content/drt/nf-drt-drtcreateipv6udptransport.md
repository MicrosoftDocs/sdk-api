---
UID: NF:drt.DrtCreateIpv6UdpTransport
title: DrtCreateIpv6UdpTransport function
author: windows-sdk-content
description: DrtCreateIpv6UdpTransport function creates a transport based on the IPv6 UDP protocol.
old-location: p2p\drtcreateipv6udptransport.htm
old-project: p2psdk
ms.assetid: def3120b-98b6-4e31-8166-822cea7fea69
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DrtCreateIpv6UdpTransport, DrtCreateIpv6UdpTransport function [Peer Networking], drt/DrtCreateIpv6UdpTransport, p2p.drtcreateipv6udptransport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
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
req.typenames: DRT_REGISTRATION_STATE, *PDRT_REGISTRATION_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtCreateIpv6UdpTransport
product: Windows
targetos: Windows
req.lib: Drttransport.lib
req.dll: Drt.dll
req.irql: 
---

# DrtCreateIpv6UdpTransport function


## -description


The <b>DrtCreateIpv6UdpTransport</b> function creates a  transport based on the IPv6 UDP protocol.


## -parameters




### -param scope

The <b>DRT_SCOPE</b> enumeration that specifies the IPv6 scope in which the DRT is to  operate.


### -param dwScopeId

The identifier that uniquely specifies the interface the scope is associated with.

For the Global scope this parameter is always the "GLOBAL_" ID and is optional when using only the global scope.
For the link local scope, this parameter represents the interface associated with the Network Interface Card on which the link local scope exists.



### -param dwLocalityThreshold

The identifier that specifies how Locality information based on IpV6 addresses is used when caching neighbors.  By default, the DRT gives preference to neighbors that have an IPv6 address with a prefix in common with the local machine.



### -param pwPort [in, out]

Pointer to the port utilized by the local DRT instance.


### -param phTransport [out]

Pointer to a DRT transport handle specified in the <a href="https://msdn.microsoft.com/22408b8e-b114-43cd-8f84-3eaf8508f441">DRT_SETTINGS</a> structure.


## -returns



This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system cannot allocate memory for the provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_PORT</b></dt>
</dl>
</td>
<td width="60%">
<i>pwPort</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_TRANSPORT_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
<i>hTransport</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_SCOPE</b></dt>
</dl>
</td>
<td width="60%">
The specified scope is not DRT_GLOBAL_SCOPE, DRT_SITE_LOCAL_SCOPE  or DRT_LINK_LOCAL_SCOPE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.  See TraceError for reason.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  This function may also return errors from underlying calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff568809">NotifyUnicastIpAddressChange</a>,<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a>, <a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a>, <a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a>, <a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a>, <a href="https://msdn.microsoft.com/0fe5a66a-1126-494c-b4da-8041841685c6">Bind</a>, <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>, <a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a>, <a href="https://msdn.microsoft.com/668593fe-2ed1-418d-8cd5-5fac61826ea1">CreateThreadpoolCleanupGroup</a> and <a href="https://msdn.microsoft.com/7d88dc0d-4650-4197-a719-01e2f5ff96df">CreateTimerQueue</a>.</div>
<div> </div>



## -remarks



The default IPv6 UDP Transport  created by this function is specific to the DRT it is created for. As a result it cannot be re-used across multiple DRTs.

When using the Distributed Routing Table API in Windows XP with Service Pack 2 (SP2), support of the IPv6 protocol must be enabled for the creation of a transport using <b>DrtCreateIpv6UdpTransport</b> to be successful.




## -see-also




<a href="https://msdn.microsoft.com/22408b8e-b114-43cd-8f84-3eaf8508f441">DRT_SETTINGS</a>



<a href="https://msdn.microsoft.com/9b078f63-36b1-448b-b0c2-d452699157d8">DrtDeleteIpv6UdpTransport</a>
 

 

