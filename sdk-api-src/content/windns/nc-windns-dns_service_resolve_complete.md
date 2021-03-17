---
UID: NC:windns.DNS_SERVICE_RESOLVE_COMPLETE
title: DNS_SERVICE_RESOLVE_COMPLETE callback function
description: Used to asynchronously return the results of a service resolve operation.
tech.root: dns
helpviewer_keywords: ["DNS_SERVICE_RESOLVE_COMPLETE"]
ms.date: 02/19/2019
ms.keywords: DNS_SERVICE_RESOLVE_COMPLETE
targetos: Windows
req.assembly: 
req.construct-type: function
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
req.typenames: DNS_SERVICE_RESOLVE_COMPLETE
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
f1_keywords:
 - DNS_SERVICE_RESOLVE_COMPLETE
 - windns/DNS_SERVICE_RESOLVE_COMPLETE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - windns.h
api_name:
 - DNS_SERVICE_RESOLVE_COMPLETE
---

## -description

Used to asynchronously return the results of a service resolve operation.

## -parameters

### -param Status

A value that contains the status associated with this particular set of results.

### -param pQueryContext

A pointer to the user context that was passed to [DnsServiceResolve](nf-windns-dnsserviceresolve.md).

### -param pInstance

A pointer to a [DNS_SERVICE_INSTANCE](ns-windns-dns_service_instance.md) structure that contains detailed information about a service on the network. If not `nullptr`, then you are responsible for freeing the data using [DnsServiceFreeInstance](nf-windns-dnsservicefreeinstance.md).

## -remarks

## -see-also

