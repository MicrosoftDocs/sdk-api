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

# in6_addr structure


## -description


The IN6_ADDR structure specifies an IPv6 transport address.


## -struct-fields




### -field u

A union that contains the following different representations of the IPv6 transport
     address:


### -field u.Byte

An array that contains 16 UCHAR-typed values.


### -field u.Word

An array that contains eight USHORT-typed values.


## -remarks



All members of the IN6_ADDR structure must be specified in network-byte-order (big-endian).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570824">SOCKADDR_IN6</a>
 

 

