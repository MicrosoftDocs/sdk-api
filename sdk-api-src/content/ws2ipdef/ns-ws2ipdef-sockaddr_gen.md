---
UID: NS:ws2ipdef.sockaddr_gen
title: sockaddr_gen (ws2ipdef.h)
description: Provides generic socket address information, and is used with the INTERFACE_INFO structure.
helpviewer_keywords: ["sockaddr_gen","sockaddr_gen union [Winsock]","winsock.sockaddr_gen","ws2ipdef/sockaddr_gen","ws2tcpip/sockaddr_gen"]
old-location: winsock\sockaddr_gen.htm
tech.root: WinSock
ms.assetid: 60b11476-07ca-476e-a2f0-669631835128
ms.date: 12/05/2018
ms.keywords: sockaddr_gen, sockaddr_gen union [Winsock], winsock.sockaddr_gen, ws2ipdef/sockaddr_gen, ws2tcpip/sockaddr_gen
req.header: ws2ipdef.h
req.include-header: Ws2tcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: sockaddr_gen
req.redist: 
ms.custom: 19H1
f1_keywords:
 - sockaddr_gen
 - ws2ipdef/sockaddr_gen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2ipdef.h
 - Ws2tcpip.h
api_name:
 - sockaddr_gen
---

# sockaddr_gen structure


## -description

The <b>sockaddr_gen</b> union provides generic socket address information, and is used with the <a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-interface_info">INTERFACE_INFO</a> structure.

## -struct-fields

### -field Address

IP address information expressed in a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure.

### -field AddressIn

IP address information expressed in a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr_in</a> structure.

### -field AddressIn6

IP address information expressed in a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr_in6_old</a> structure.

## -remarks

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>sockaddr_gen</b> union is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.

## -see-also

<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr_in</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr_in6_old</a>