---
UID: NF:windns.DnsServiceBrowse
title: DnsServiceBrowse function
description: Used to initiate a DNS-SD discovery for services running on the local network.
tech.root: dns
helpviewer_keywords: ["DnsServiceBrowse"]
ms.date: 02/14/2019
ms.keywords: DnsServiceBrowse
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
 - DnsServiceBrowse
 - windns/DnsServiceBrowse
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - windns.h
api_name:
 - DnsServiceBrowse
---

## -description

Used to initiate a DNS-SD discovery for services running on the local network.

## -parameters

### -param pRequest

A pointer to a [DNS_SERVICE_BROWSE_REQUEST](ns-windns-dns_service_browse_request.md) structure that contains the browse request information.

### -param pCancel

A pointer to a [DNS_SERVICE_CANCEL](ns-windns-dns_service_cancel.md) structure that can be used to cancel a pending asynchronous browsing operation. This handle must remain valid until the query is canceled.

## -returns

If successful, returns **DNS_REQUEST_PENDING**; otherwise, returns the appropriate DNS-specific error code as defined in `Winerror.h`. For extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

This function is asynchronous. As services are being discovered, the browse callback will be invoked for each result.

## -see-also