---
UID: NS:windns._DNS_SERVICE_BROWSE_REQUEST
title: DNS_SERVICE_BROWSE_REQUEST structure
description: Contains the query parameters used in a call to [DnsServiceBrowse](nf-windns-dnsservicebrowse.md).
ms.date: 02/19/2019
ms.keywords: _DNS_SERVICE_BROWSE_REQUEST, DNS_SERVICE_BROWSE_REQUEST
ms.topic: language-reference
f1_keywords: 
 - "windns/_DNS_SERVICE_BROWSE_REQUEST"
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
req.typenames: DNS_SERVICE_BROWSE_REQUEST, *PDNS_SERVICE_BROWSE_REQUEST
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - _DNS_SERVICE_BROWSE_REQUEST
 - DNS_SERVICE_BROWSE_REQUEST
ms.custom: 19H1
---

## -description
Contains the query parameters used in a call to [DnsServiceBrowse](nf-windns-dnsservicebrowse.md).

## -struct-fields

### -field Version
The structure version must be either **DNS_QUERY_REQUEST_VERSION1** or **DNS_QUERY_REQUEST_VERSION2**. The value determines which of `pBrowseCallback` or `pBrowseCallbackV2` is active.

### -field InterfaceIndex
A value that contains the interface index over which the query is sent. If `InterfaceIndex` is 0, then all interfaces will be considered.

### -field QueryName
A pointer to a string that represents the service type whose matching services you wish to browse for. It takes the generalized form "\_\<ServiceType\>.\_\<TransportProtocol\>.local". For example, "_http._tcp.local", which defines a query to browse for http services on the local link.

### -field pBrowseCallback
A pointer to a function (of type [DNS_SERVICE_BROWSE_CALLBACK](nc-windns-dns_service_browse_callback.md)) that represents the callback to be invoked asynchronously. This field is used if `Version` is **DNS_QUERY_REQUEST_VERSION1**.

### -field pBrowseCallbackV2
A pointer to a function (of type [DNS_QUERY_COMPLETION_ROUTINE](nc-windns-dns_query_completion_routine.md)) that represents the callback to be invoked asynchronously. This field is used if `Version` is **DNS_QUERY_REQUEST_VERSION2**.

### -field pQueryContext
A pointer to a user context.

## -remarks

## -see-also
