---
UID: NS:windns._DNS_SERVICE_RESOLVE_REQUEST
title: DNS_SERVICE_RESOLVE_REQUEST structure
description: Contains the query parameters used in a call to [DnsServiceResolve](../windns/nf-windns-dnsserviceresolve.md).
tech.root: dns
helpviewer_keywords: ["_DNS_SERVICE_RESOLVE_REQUEST","DNS_SERVICE_RESOLVE_REQUEST"]
ms.date: 02/19/2019
ms.keywords: _DNS_SERVICE_RESOLVE_REQUEST, DNS_SERVICE_RESOLVE_REQUEST
targetos: Windows
req.assembly: 
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: windns.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.typenames: DNS_SERVICE_RESOLVE_REQUEST, *PDNS_SERVICE_RESOLVE_REQUEST
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
f1_keywords:
 - _DNS_SERVICE_RESOLVE_REQUEST
 - windns/_DNS_SERVICE_RESOLVE_REQUEST
 - PDNS_SERVICE_RESOLVE_REQUEST
 - windns/PDNS_SERVICE_RESOLVE_REQUEST
 - DNS_SERVICE_RESOLVE_REQUEST
 - windns/DNS_SERVICE_RESOLVE_REQUEST
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - _DNS_SERVICE_RESOLVE_REQUEST
 - DNS_SERVICE_RESOLVE_REQUEST
---

## -description

Contains the query parameters used in a call to [DnsServiceResolve](/windows/win32/api/windns/nf-windns-dnsserviceresolve). Use that function, and this structure, after you've found a specific service name that you'd like to connect to.

## -struct-fields

### -field Version

The structure version must be **DNS_QUERY_REQUEST_VERSION1**.

### -field InterfaceIndex

A value that contains the interface index over which the query is sent. If `InterfaceIndex` is 0, then all interfaces will be considered.

### -field QueryName

A pointer to a string that represents the service name. This is a fully qualified domain name that begins with a service name, and ends with ".local". It takes the generalized form "\<ServiceName\>.\_\<ServiceType\>.\_\<TransportProtocol\>.local". For example, "MyMusicServer._http._tcp.local".

### -field pResolveCompletionCallback

A pointer to a function (of type [DNS_SERVICE_RESOLVE_COMPLETE](nc-windns-dns_service_resolve_complete.md)) that represents the callback to be invoked asynchronously.

### -field pQueryContext

A pointer to a user context.

## -remarks

## -see-also

