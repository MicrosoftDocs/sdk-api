---
UID: NS:in6addr.in6_addr
title: in6_addr
author: windows-driver-content
description: The IN6_ADDR structure specifies an IPv6 transport address.
old-location: netvista\in6_addr.htm
old-project: netvista
ms.assetid: 218b07e8-94cf-42f2-a762-13fc1f7c4473
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: "*LPIN6_ADDR, *PIN6_ADDR, IN6_ADDR, IN6_ADDR structure [Network Drivers Starting with Windows Vista], LPIN6_ADDR, LPIN6_ADDR structure pointer [Network Drivers Starting with Windows Vista], PIN6_ADDR, PIN6_ADDR structure pointer [Network Drivers Starting with Windows Vista], in6_addr, in6addr/IN6_ADDR, in6addr/LPIN6_ADDR, in6addr/PIN6_ADDR, netvista.in6_addr, wskref_fd9f043f-fd21-4d2e-b683-0437cf3523c1.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: in6addr.h
req.include-header: Ws2ipdef.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
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
req.typenames: IN6_ADDR, *PIN6_ADDR, *LPIN6_ADDR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	in6addr.h
api_name:
-	IN6_ADDR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# in6_addr structure


## -description


The IN6_ADDR structure specifies an IPv6 transport address.


## -struct-fields




### -field u

A union that contains the following different representations of the IPv6 transport
     address:



#### Byte

An array that contains 16 UCHAR-typed values.



#### Word

An array that contains eight USHORT-typed values.


## -remarks



All members of the IN6_ADDR structure must be specified in network-byte-order (big-endian).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570824">SOCKADDR_IN6</a>
 

 

