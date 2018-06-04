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

# DNS_PROXY_INFORMATION structure


## -description


The <b>DNS_PROXY_INFORMATION</b> structure  contains the proxy information for a DNS server's name resolution policy table.


## -struct-fields




### -field version

A value that specifies the structure version. This value must be 1.


### -field proxyInformationType

A <a href="https://msdn.microsoft.com/983d38f3-3ee7-4df6-a9ff-f908f250020f">DNS_PROXY_INFORMATION_TYPE</a> enumeration that contains the proxy information type.


### -field proxyName

A pointer to a string that contains the proxy server name if <b>proxyInformationType</b> is <b>DNS_PROXY_INFORMATION_PROXY_NAME</b>. Otherwise, this member is ignored.

<div class="alert"><b>Note</b>  To free this string, use the 
<a href="https://msdn.microsoft.com/4c69d548-3bb5-4609-9fc5-3a829a285956">DnsFreeProxyName</a> function.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/636399be-43a5-4ddf-b652-f8efb81fbf42">DNS Structures</a>



<a href="https://msdn.microsoft.com/fdc8eb09-e071-4f03-974a-2b11a657ab18">DnsGetProxyInformation</a>
 

 

