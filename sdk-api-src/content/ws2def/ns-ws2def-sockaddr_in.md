---
UID: NS:ws2def.sockaddr_in
title: SOCKADDR_IN (ws2def.h)
description: The SOCKADDR_IN structure specifies a transport address and port for the AF_INET address family.
helpviewer_keywords: ["*PSOCKADDR_IN","PSOCKADDR_IN","PSOCKADDR_IN structure pointer [Network Drivers Starting with Windows Vista]","SOCKADDR_IN","SOCKADDR_IN structure [Network Drivers Starting with Windows Vista]","netvista.sockaddr_in","ws2def/PSOCKADDR_IN","ws2def/SOCKADDR_IN","wskref_ab4750b0-daae-4326-91a3-a94a9863c7a2.xml"]
old-location: netvista\sockaddr_in.htm
tech.root: NetVista
ms.assetid: 96379562-403f-451c-ac7a-f0eec34bfe5e
ms.date: 12/05/2018
ms.keywords: '*PSOCKADDR_IN, PSOCKADDR_IN, PSOCKADDR_IN structure pointer [Network Drivers Starting with Windows Vista], SOCKADDR_IN, SOCKADDR_IN structure [Network Drivers Starting with Windows Vista], netvista.sockaddr_in, ws2def/PSOCKADDR_IN, ws2def/SOCKADDR_IN, wskref_ab4750b0-daae-4326-91a3-a94a9863c7a2.xml'
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
targetos: Windows
req.typenames: SOCKADDR_IN, *PSOCKADDR_IN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - sockaddr_in
 - ws2def/sockaddr_in
 - PSOCKADDR_IN
 - ws2def/PSOCKADDR_IN
 - SOCKADDR_IN
 - ws2def/SOCKADDR_IN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ws2def.h
api_name:
 - SOCKADDR_IN
---

# SOCKADDR_IN structure


## -description

The SOCKADDR_IN structure specifies a transport address and port for the 
  <a href="/windows-hardware/drivers/network/af-inet">AF_INET</a> address family.

## -struct-fields

### -field sin_family

The address family for the transport address. This member should always be set to AF_INET.

### -field sin_port

A transport protocol port number.

### -field sin_addr

An 
     <a href="/previous-versions/windows/hardware/drivers/ff556972(v=vs.85)">IN_ADDR</a> structure that contains an IPv4 transport
     address.

### -field sin_zero

Reserved for system use. A WSK application should set the contents of this array to zero.

## -remarks

All of the data in the SOCKADDR_IN structure, except for the address family, must be specified in
    network-byte-order (big-endian).

## -see-also

<a href="/windows-hardware/drivers/network/af-inet">AF_INET</a>



<a href="/previous-versions/windows/hardware/drivers/ff556972(v=vs.85)">IN_ADDR</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-sockaddr">SOCKADDR</a>



[SOCKADDR_STORAGE](./ns-ws2def-sockaddr_storage_lh.md)