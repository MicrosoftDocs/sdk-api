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

# DnsFree function


## -description


The <b>DnsFree</b> function frees memory allocated for DNS records that was obtained using the 
<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a> function.


## -parameters




### -param pData [in, out]

A pointer to the DNS data to be freed.


### -param FreeType [in]

A value that specifies the type of DNS data in <i>pData</i>. For more information and a list of values, see the <a href="https://msdn.microsoft.com/976982a1-08f1-4c67-b823-1eea34f0c643">DNS_FREE_TYPE</a> enumeration.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/976982a1-08f1-4c67-b823-1eea34f0c643">DNS_FREE_TYPE</a>
 

 

