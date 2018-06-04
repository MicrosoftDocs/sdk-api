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

# _DnsAddrArray structure


## -description


The <b>DNS_ADDR_ARRAY</b> structure stores an array of IPv4 or IPv6 addresses.


## -struct-fields




### -field MaxCount

Indicates, the size, in bytes,  of this structure.


### -field AddrCount

Indicates the number of <a href="https://msdn.microsoft.com/c14e6fc0-34b3-40e8-b9b8-61e4aea01677">DNS_ADDR</a> structures contained in the <b>AddrArray</b> member.


### -field Tag

Reserved. Do not use.


### -field Family

A value that specifies the IP family. Possible values are:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
</dl>
</td>
<td width="60%">
IPv6

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
</dl>
</td>
<td width="60%">
IPv4

</td>
</tr>
</table>
 


### -field WordReserved

Reserved. Do not use.


### -field Flags

Reserved. Do not use.


### -field MatchFlag

Reserved. Do not use.


### -field Reserved1

Reserved. Do not use.


### -field Reserved2

Reserved. Do not use.


### -field AddrArray

An array of <a href="https://msdn.microsoft.com/c14e6fc0-34b3-40e8-b9b8-61e4aea01677">DNS_ADDR</a> structures that each contain an IP address.


### -field AddrArray.size_is

 


### -field AddrArray.size_is.AddrCount

 




## -see-also




<a href="https://msdn.microsoft.com/c14e6fc0-34b3-40e8-b9b8-61e4aea01677">DNS_ADDR</a>



<a href="https://msdn.microsoft.com/03EB1DC2-FAB0-45C5-B438-E8FFDD218F09">DNS_QUERY_RESULT</a>
 

 

