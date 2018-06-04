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

# IBDA_IPV4Filter::GetMulticastListSize


## -description



The <b>GetMulticastListSize</b> method retrieves the number of addresses in the list.




## -parameters




### -param pulcbAddresses [in, out]

Pointer that receives the number of addresses multiplied by the size of an IPv4 address.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is used by an IPv4 Network Data Sink filter to request that a Network Provider make its best effort to tune to the stream(s) on which a list of IPv4 multicast addresses may be transmitted. Addresses in the address list are byte-aligned in Network order. <i>UlcbAddresses</i> will always be an integer multiple of the size of an IPv4 address.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3db86e21-6d05-4b7f-be83-a3fa506a0e3b">IBDA_IPV4Filter Interface</a>
 

 

