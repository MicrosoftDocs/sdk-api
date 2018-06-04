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

# sockaddr_gen structure


## -description


The <b>sockaddr_gen</b> union provides generic socket address information, and is used with the <a href="https://msdn.microsoft.com/fe1bf38d-70a7-4f0a-b76a-c0c9443d1782">INTERFACE_INFO</a> structure.


## -struct-fields




### -field Address

IP address information expressed in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure.


### -field AddressIn

IP address information expressed in a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570823">sockaddr_in</a> structure.


### -field AddressIn6

IP address information expressed in a <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr_in6_old</a> structure.


## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>sockaddr_gen</b> union is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570823">sockaddr_in</a>



<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr_in6_old</a>
 

 

