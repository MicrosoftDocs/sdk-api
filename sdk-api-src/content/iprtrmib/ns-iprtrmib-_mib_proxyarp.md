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

# _MIB_PROXYARP structure


## -description


The 
<b>MIB_PROXYARP</b> structure stores information for a Proxy Address Resolution Protocol (PARP) entry.


## -struct-fields




### -field dwAddress

The IPv4 address for which to act as a proxy.


### -field dwMask

The subnet mask for the IPv4 address specified by the <b>dwAddress</b> member.


### -field dwIfIndex

The index of the interface on which to act as a proxy for the address specified by the <b>dwAddress</b> member.


## -see-also




<a href="_iphlp_createproxyarpentry">CreateProxyArpEntry</a>



<a href="_iphlp_deleteproxyarpentry">DeleteProxyArpEntry</a>
 

 

