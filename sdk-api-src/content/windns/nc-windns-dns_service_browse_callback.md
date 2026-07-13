---
UID: NC:windns.DNS_SERVICE_BROWSE_CALLBACK
title: DNS_SERVICE_BROWSE_CALLBACK callback function
description: Used to asynchronously return the results of a DNS-SD query.
tech.root: dns
helpviewer_keywords: ["DNS_SERVICE_BROWSE_CALLBACK"]
ms.date: 02/19/2019
ms.keywords: DNS_SERVICE_BROWSE_CALLBACK
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
req.typenames: DNS_SERVICE_BROWSE_CALLBACK
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
f1_keywords:
 - DNS_SERVICE_BROWSE_CALLBACK
 - windns/DNS_SERVICE_BROWSE_CALLBACK
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - windns.h
api_name:
 - DNS_SERVICE_BROWSE_CALLBACK
---

## -description

Used to asynchronously return the results of a DNS-SD query.

## -parameters

### -param Status

A value that contains the status associated with this particular set of results.

### -param pQueryContext

A pointer to the user context that was passed to [DnsServiceBrowse](nf-windns-dnsservicebrowse.md).

### -param pDnsRecord

A pointer to a [DNS_RECORD](./ns-windnsdef-dns_recordw.md) structure that contains a list of records describing a discovered service on the network. If not `nullptr`, then you are responsible for freeing the returned RR sets using [DnsRecordListFree](/windows/desktop/api/windns/nf-windns-dnsrecordlistfree).

## -remarks

## -see-also