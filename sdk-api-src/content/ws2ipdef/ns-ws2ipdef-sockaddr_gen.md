---
UID: NS:ws2ipdef.sockaddr_gen
title: sockaddr_gen
author: windows-driver-content
description: Provides generic socket address information, and is used with the INTERFACE_INFO structure.
old-location: winsock\sockaddr_gen.htm
old-project: WinSock
ms.assetid: 60b11476-07ca-476e-a2f0-669631835128
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: sockaddr_gen, sockaddr_gen union [Winsock], winsock.sockaddr_gen, ws2ipdef/sockaddr_gen, ws2tcpip/sockaddr_gen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ws2ipdef.h
req.include-header: Ws2tcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: sockaddr_gen
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ws2ipdef.h
-	Ws2tcpip.h
api_name:
-	sockaddr_gen
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

