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

# sockaddr_in structure


## -description


The SOCKADDR_IN structure specifies a transport address and port for the 
  <a href="https://msdn.microsoft.com/library/windows/hardware/ff543744">AF_INET</a> address family.


## -struct-fields




### -field sin_family

The address family for the transport address. This member should always be set to AF_INET.


### -field sin_port

A transport protocol port number.


### -field sin_addr

An 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">IN_ADDR</a> structure that contains an IPv4 transport
     address.


### -field sin_zero

Reserved for system use. A WSK application should set the contents of this array to zero.


## -remarks



All of the data in the SOCKADDR_IN structure, except for the address family, must be specified in
    network-byte-order (big-endian).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543744">AF_INET</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">IN_ADDR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a>
 

 

