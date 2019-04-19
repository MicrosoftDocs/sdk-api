---
UID: NF:windns.DnsServiceResolve
title: DnsServiceResolve function
description: Used to obtain more information about a service advertised on the local network.
ms.date: 02/14/2019
ms.keywords: DnsServiceResolve
ms.topic: language-reference
targetos: Windows
product: Windows
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
topic_type:
 - apiref
api_type:
 - 
api_location:
 - windns.h
api_name:
 - DnsServiceResolve
ms.custom: 19H1
---

## -description
Used to obtain more information about a service advertised on the local network.

## -parameters

### -param pRequest
A pointer to a [DNS_SERVICE_RESOLVE_REQUEST](ns-windns-dns_service_resolve_request.md) structure that contains the resolve request information.

### -param pCancel
A pointer to a [DNS_SERVICE_CANCEL](ns-windns-dns_service_cancel.md) structure that can be used to cancel a pending asynchronous resolve operation. This handle must remain valid until the query is canceled.

## -returns
If successful, returns **DNS_REQUEST_PENDING**; otherwise, returns the appropriate DNS-specific error code as defined in `Winerror.h`. For extended error information, call [GetLastError](https://msdn.microsoft.com/library/ms679360).

## -remarks
This function is asynchronous. Upon completion, the resolve callback will be invoked for each result. In contrast to [DnsServiceBrowse](nf-windns-dnsservicebrowse.md)&mdash;which returns the service name as a minimum&mdash;**DnsServiceResolve** can be used to retrieve additional information, such as hostname, IP address, and TEXT records.

## -see-also
