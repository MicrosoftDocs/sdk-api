---
UID: NS:in6addr.in6_addr
title: in6_addr
author: windows-driver-content
description: The in6_addr structure represents an IPv6 address.
old-location: winsock\in6_addr.htm
old-project: WinSock
ms.assetid: 2029db76-3fe1-4560-b753-910c48cbc578
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: "*LPIN6_ADDR, *PIN6_ADDR, FAR *LPIN6_ADDR, FAR *LPIN6_ADDR structure [Winsock], IN6_ADDR, IN6_ADDR [Winsock], IN6_ADDR structure [Winsock], PIN6_ADDR, PIN6_ADDR structure pointer [Winsock], in6_addr, in6_addr structure [Winsock], in6addr/FAR *LPIN6_ADDR, in6addr/PIN6_ADDR, in6addr/in6_addr, winsock.in6_addr, ws2tcpip/FAR *LPIN6_ADDR, ws2tcpip/PIN6_ADDR, ws2tcpip/in6_addr"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: in6addr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
-	In6addr.h
-	Ws2tcpip.h
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


The 
<b>in6_addr</b> structure represents an IPv6 address.


## -struct-fields




### -field u



#### Byte

An IPv6 address formatted as an array of sixteen <b>u_char</b>s.



#### Word

An IPv6 address formatted as an array of eight <b>u_short</b>s.


## -remarks



The <b>in6_addr</b> structure is used with IPv6 addresses. 

The <b>in6_addr</b> structure is the IPv6 equivalent of the IPv4-based <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a> structure.  

<div class="alert"><b>Note</b>  The <b>IN6_ADDR</b>, <b>PIN6_ADDR</b>, and  <b>LPIN6_ADDR</b> derived structures are only defined on the Windows SDK released with Windows Vista and later. The <b>IN6_ADDR</b>, <b>PIN6_ADDR</b>, and  <b>LPIN6_ADDR</b> derived structures are defined in the <i>In6addr.h</i> header file. The <b>in6_addr</b> structure should be used on earlier versions of the Windows SDK. </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">SOCKADDR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a>



<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a>
 

 

