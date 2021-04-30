---
UID: NF:windns.DnsServiceCopyInstance
title: DnsServiceCopyInstance function
description: Used to copy a [DNS_SERVICE_INSTANCE](../windns/ns-windns-dns_service_instance.md) structure.
tech.root: dns
helpviewer_keywords: ["DnsServiceCopyInstance"]
ms.date: 02/19/2019
ms.keywords: DnsServiceCopyInstance
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: dnsapi.dll
req.header: windns.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: dnsapi.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
f1_keywords:
 - DnsServiceCopyInstance
 - windns/DnsServiceCopyInstance
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - windns.h
api_name:
 - DnsServiceCopyInstance
---

## -description

Used to copy a [DNS_SERVICE_INSTANCE](/windows/win32/api/windns/ns-windns-dns_service_instance) structure.

## -parameters

### -param pOrig

A pointer to the [DNS_SERVICE_INSTANCE](ns-windns-dns_service_instance.md) structure that is to be copied.

## -returns

A pointer to a newly allocated [DNS_SERVICE_INSTANCE](ns-windns-dns_service_instance.md) structure that's a copy of `pOrig`. Your application is responsible for freeing the associated memory by calling [DnsServiceFreeInstance](nf-windns-dnsservicefreeinstance.md).

## -remarks

## -see-also

