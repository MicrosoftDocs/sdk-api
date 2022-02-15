---
UID: NS:ws2def.addrinfo_dns_server
title: ADDRINFO_DNS_SERVER
description: Represents a custom Domain Name System (DNS) server, used in the Winsock APIs.
tech.root: WinSock
ms.date: 06/14/2021
prerelease: false
req.construct-type: structure
req.header: ws2def.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
req.typenames: ADDRINFO_DNS_SERVER
req.redist: 
f1_keywords:
 - addrinfo_dns_server
 - ws2def/addrinfo_dns_server
 - ADDRINFO_DNS_SERVER
 - ws2def/ADDRINFO_DNS_SERVER
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
 - addrinfo_dns_server
 - ADDRINFO_DNS_SERVER
---

## -description

Represents a custom Domain Name System (DNS) server, used in the Winsock APIs.

## -struct-fields

### -field ai_servertype

The type of DNS server. Can be one of the following values.

| Constant                   | Value  | Meaning                    |
|----------------------------|--------|----------------------------|
| **AI_DNS_SERVER_TYPE_UDP** | 1      | A regular DNS server.      |
| **AI_DNS_SERVER_TYPE_DOH** | 2      | A *DNS-over-HTTPS* server. |

### -field ai_flags

A bitmap containing any of the following options.

| Constant | Value | Meaning |
|-|-|-|
| **AI_DNS_SERVER_UDP_FALLBACK** | 0x1 | This server can also be used for non-secure name resolution. |

### -field ai_addrlen

The length in bytes of the socket address structure that *ai_addr* points to.

### -field ai_addr

A pointer to a socket address structure containing the address of the custom server. Only **SOCKADDR_IN** and **SOCKADDR_IN6** structures are supported. The *sa_family* member must be set to **AF_INET** or **AF_INET6**. The rest of the structure must be zeroed out, with the exception of the **SOCKADDR_IN::sin_addr** member for IPv4, or **SOCKADDR_IN6::sin6_addr** for IPv6.

### -field ai_template

If *ai_servertype* is set to **AI_DNS_SERVER_TYPE_DOH**, then this member must point to a **NULL**-terminated wide string representing the *DNS-over-HTTPS* template for this server.

If *ai_servertype* is set to **AI_DNS_SERVER_TYPE_UDP**, then this field must be **NULL**.

## -remarks

## -see-also

* [ADDRINFOEX6](/windows/win32/api/ws2def/ns-ws2def-addrinfoex6)
