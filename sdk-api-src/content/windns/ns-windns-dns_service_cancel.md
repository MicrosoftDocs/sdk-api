---
UID: NS:windns._DNS_SERVICE_CANCEL
title: DNS_SERVICE_CANCEL structure
description: Used to cancel an asynchronous DNS-SD operation.
tech.root: dns
helpviewer_keywords: ["_DNS_SERVICE_CANCEL","DNS_SERVICE_CANCEL"]
ms.date: 02/19/2019
ms.keywords: _DNS_SERVICE_CANCEL, DNS_SERVICE_CANCEL
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
req.typenames: DNS_SERVICE_CANCEL, *PDNS_SERVICE_CANCEL
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
f1_keywords:
 - _DNS_SERVICE_CANCEL
 - windns/_DNS_SERVICE_CANCEL
 - PDNS_SERVICE_CANCEL
 - windns/PDNS_SERVICE_CANCEL
 - DNS_SERVICE_CANCEL
 - windns/DNS_SERVICE_CANCEL
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - _DNS_SERVICE_CANCEL
 - DNS_SERVICE_CANCEL
---

## -description

Used to cancel an asynchronous DNS-SD operation.

## -struct-fields

### -field reserved

Contains a handle associated with the asynchronous operation to cancel. Your application must not modify this value.

## -remarks

This structure is returned in the `pCancel` parameter from a previous call to [DnsServiceBrowse](nf-windns-dnsservicebrowse.md), [DnsServiceRegister](nf-windns-dnsserviceregister.md), or [DnsServiceResolve](nf-windns-dnsserviceresolve.md).

## -see-also

