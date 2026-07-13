---
UID: NS:windnsdef._DNS_CUSTOM_SERVER
title: DNS_CUSTOM_SERVER
description: Represents a DNS custom server. A **DNS_CUSTOM_SERVER** object is passed to [DnsQueryEx](/windows/win32/api/windnsdef/nf-windns-dnsqueryex) via the [DNS_QUERY_REQUEST3](/windows/win32/api/windnsdef/ns-windns-dns_query_request3) structure.
tech.root: DNS
ms.date: 05/28/2021
prerelease: false
req.construct-type: structure
req.header: windnsdef.h
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
req.typenames: DNS_CUSTOM_SERVER
req.redist: 
f1_keywords:
 - _DNS_CUSTOM_SERVER
 - windnsdef/_DNS_CUSTOM_SERVER
 - DNS_CUSTOM_SERVER
 - windnsdef/DNS_CUSTOM_SERVER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - _DNS_CUSTOM_SERVER
 - DNS_CUSTOM_SERVER
---

## -description

Represents a DNS custom server. A **DNS_CUSTOM_SERVER** object is passed to [DnsQueryEx](/windows/win32/api/windnsdef/nf-windns-dnsqueryex) via the [DNS_QUERY_REQUEST3](/windows/win32/api/windnsdef/ns-windns-dns_query_request3) structure.

To use **DNS_CUSTOM_SERVER** together with *ServerAddr*, include `ws2ipdef.h` before `windns.h`.

## -struct-fields

### -field dwServerType

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The server type. Must be one of the following.

||Value|Description|
|-|-|-|
|**DNS_CUSTOM_SERVER_TYPE_UDP**|0x1|Perform unsecure name resolution|
|**DNS_CUSTOM_SERVER_TYPE_DOH**|0x2|Perform **DNS-over-HTTPS** name resolution|

### -field ullFlags

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

A value that contains a bitmap of the following options.

||Value|Description|
|-|-|-|
|**DNS_CUSTOM_SERVER_UDP_FALLBACK**|0x1|Server might fall back to unsecure resolution|

### -field pwszTemplate

Type: **[PWSTR](/windows/win32/winprog/windows-data-types)**

A **NULL**-terminated wide string representing the **DNS-over-HTTPS** template.

If *dwServerType* is set to **DNS_CUSTOM_SERVER_TYPE_UDP**, then this field must be **NULL**.

If *dwServerType* is set to **DNS_CUSTOM_SERVER_TYPE_DOH**, then this field must point to a valid **NULL**-terminated string.

### -field ServerAddr

Type: **[SOCKADDR_INET](/windows/win32/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet)**

A [SOCKADDR_INET](/windows/win32/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet) object containing the address of the custom DNS server. Only an address family of **AF_INET** or **AF_INET6** is supported. If the address family is set to **AF_INET**, then the **Ipv4.sin_addr** member must be set to a valid IPv4 address. If the address family is set to **AF_INET6**, then the **Ipv6.sin6_addr** member must be set to a valid IPv6 address. The remainder of the fields must be zeroed out.

### -field MaxSa

Type: **[CHAR](/windows/win32/winprog/windows-data-types)\[DNS\_ADDR\_MAX\_SOCKADDR\_LENGTH\]**

A byte array, which designates storage for a [SOCKADDR_INET](/windows/win32/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet). *MaxSa* is a union with *ServerAddr*.

To use **DNS_CUSTOM_SERVER** together with *ServerAddr*, you must include `ws2ipdef.h` before `windns.h`.

Besides storage for the **SOCKADDR_INET**, *MaxSa* avoids compile errors caused by *not* including `ws2ipdef.h`. This allows you to use any functionality from `windns.h` except for the **DNS_CUSTOM_SERVER**.

## -remarks

## -see-also

* [DnsQueryEx function](/windows/win32/api/windnsdef/nf-windns-dnsqueryex)
* [DNS_QUERY_REQUEST3 structure](/windows/win32/api/windnsdef/ns-windns-dns_query_request3)
