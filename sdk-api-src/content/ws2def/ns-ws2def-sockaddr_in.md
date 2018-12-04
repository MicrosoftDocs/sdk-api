---
UID: NS:ws2def.sockaddr_in
title: sockaddr_in
author: windows-sdk-content
description: The SOCKADDR_IN structure specifies a transport address and port for the AF_INET address family.
old-location: netvista\sockaddr_in.htm
tech.root: NetVista
ms.assetid: 96379562-403f-451c-ac7a-f0eec34bfe5e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: "*PSOCKADDR_IN, PSOCKADDR_IN, PSOCKADDR_IN structure pointer [Network Drivers Starting with Windows Vista], SOCKADDR_IN, SOCKADDR_IN structure [Network Drivers Starting with Windows Vista], netvista.sockaddr_in, sockaddr_in, ws2def/PSOCKADDR_IN, ws2def/SOCKADDR_IN, wskref_ab4750b0-daae-4326-91a3-a94a9863c7a2.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ws2def.h
req.include-header: Wsk.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ws2def.h
api_name:
 - SOCKADDR_IN
product: Windows
targetos: Windows
req.typenames: SOCKADDR_IN, *PSOCKADDR_IN
req.redist: 
---

# sockaddr_in structure


## -description


The SOCKADDR_IN structure specifies a transport address and port for the 
  <a href="netvista.af_inet">AF_INET</a> address family.


## -struct-fields




### -field sin_family

The address family for the transport address. This member should always be set to AF_INET.


### -field sin_port

A transport protocol port number.


### -field sin_addr

An 
     <a href="https://msdn.microsoft.com/574c43bc-1a14-41dc-bbf8-3cb0aeb92465">IN_ADDR</a> structure that contains an IPv4 transport
     address.


### -field sin_zero

Reserved for system use. A WSK application should set the contents of this array to zero.


## -remarks



All of the data in the SOCKADDR_IN structure, except for the address family, must be specified in
    network-byte-order (big-endian).




## -see-also




<a href="netvista.af_inet">AF_INET</a>



<a href="https://msdn.microsoft.com/574c43bc-1a14-41dc-bbf8-3cb0aeb92465">IN_ADDR</a>



<a href="https://msdn.microsoft.com/af5ad9ae-3987-4f16-a8a6-14e3e3d0fa6a">SOCKADDR</a>



<a href="https://msdn.microsoft.com/27e56c1a-ce11-4cdb-9be8-25ed2f94fb37">SOCKADDR_STORAGE</a>
 

 

