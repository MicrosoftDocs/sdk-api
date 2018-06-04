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

# IUPnPAddressFamilyControl::GetAddressFamily


## -description


The <b>GetAddressFamily</b> method retrieves the current value of the address family flag of the Device Finder object.


## -parameters




### -param pdwFlags [out, retval]

Pointer to an integer (4-byte value) that indicates the address family.

The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UPNP_ADDRESSFAMILY_IPv4"></a><a id="upnp_addressfamily_ipv4"></a><a id="UPNP_ADDRESSFAMILY_IPV4"></a><dl>
<dt><b>UPNP_ADDRESSFAMILY_IPv4</b></dt>
</dl>
</td>
<td width="60%">
IPv4 (IP version 4)

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_ADDRESSFAMILY_IPv6"></a><a id="upnp_addressfamily_ipv6"></a><a id="UPNP_ADDRESSFAMILY_IPV6"></a><dl>
<dt><b>UPNP_ADDRESSFAMILY_IPv6</b></dt>
</dl>
</td>
<td width="60%">
IPv6 (IP version 6)

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_ADDRESSFAMILY_BOTH"></a><a id="upnp_addressfamily_both"></a><dl>
<dt><b>UPNP_ADDRESSFAMILY_BOTH</b></dt>
</dl>
</td>
<td width="60%">
IPv4 and IPv6

</td>
</tr>
</table>
 


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/fad61b7f-b9da-4a1b-bb5e-ad20bc87fb5c">IUPnPAddressFamilyControl</a>



<a href="https://msdn.microsoft.com/2b3e5dae-68c0-431b-bef0-fa2bb5f53bdc">SetAddressFamily</a>
 

 

