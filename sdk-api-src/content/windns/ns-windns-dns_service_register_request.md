---
UID: NS:windns._DNS_SERVICE_REGISTER_REQUEST
title: DNS_SERVICE_REGISTER_REQUEST structure
description: Contains the information necessary to advertise a service using [DnsServiceRegister](../windns/nf-windns-dnsserviceregister.md), or to stop advertising it using [DnsServiceDeRegister](../windns/nf-windns-dnsservicederegister.md).
tech.root: dns
helpviewer_keywords: ["_DNS_SERVICE_REGISTER_REQUEST","DNS_SERVICE_REGISTER_REQUEST"]
ms.date: 02/19/2019
ms.keywords: _DNS_SERVICE_REGISTER_REQUEST, DNS_SERVICE_REGISTER_REQUEST
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
req.typenames: DNS_SERVICE_REGISTER_REQUEST, *PDNS_SERVICE_REGISTER_REQUEST
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
f1_keywords:
 - _DNS_SERVICE_REGISTER_REQUEST
 - windns/_DNS_SERVICE_REGISTER_REQUEST
 - PDNS_SERVICE_REGISTER_REQUEST
 - windns/PDNS_SERVICE_REGISTER_REQUEST
 - DNS_SERVICE_REGISTER_REQUEST
 - windns/DNS_SERVICE_REGISTER_REQUEST
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - _DNS_SERVICE_REGISTER_REQUEST
 - DNS_SERVICE_REGISTER_REQUEST
---

## -description

Contains the information necessary to advertise a service using [DnsServiceRegister](/windows/win32/api/windns/nf-windns-dnsserviceregister), or to stop advertising it using [DnsServiceDeRegister](/windows/win32/api/windns/nf-windns-dnsservicederegister).

## -struct-fields

### -field Version

The structure version must be **DNS_QUERY_REQUEST_VERSION1**.

### -field InterfaceIndex

A value that contains the interface index over which the service is to be advertised. If `InterfaceIndex` is 0, then all interfaces will be considered.

### -field pServiceInstance

A pointer to a [DNS_SERVICE_INSTANCE](ns-windns-dns_service_instance.md) structure that describes the service to be registered.

### -field pRegisterCompletionCallback

A pointer to a function (of type [DNS_SERVICE_REGISTER_COMPLETE](nc-windns-dns_service_register_complete.md)) that represents the callback to be invoked asynchronously.

### -field pQueryContext

A pointer to a user context.

### -field hCredentials

Not used.

### -field unicastEnabled

`true` if the DNS protocol should be used to advertise the service; `false` if the mDNS protocol should be used.

## -remarks

## -see-also

