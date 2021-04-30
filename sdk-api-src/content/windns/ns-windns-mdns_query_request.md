---
UID: NS:windns._MDNS_QUERY_REQUEST
title: MDNS_QUERY_REQUEST structure
description: Contains the necessary information to perform an mDNS query.
tech.root: dns
helpviewer_keywords: ["_MDNS_QUERY_REQUEST","MDNS_QUERY_REQUEST"]
ms.date: 02/19/2019
ms.keywords: _MDNS_QUERY_REQUEST, MDNS_QUERY_REQUEST
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
req.typenames: MDNS_QUERY_REQUEST, *PMDNS_QUERY_REQUEST
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
f1_keywords:
 - _MDNS_QUERY_REQUEST
 - windns/_MDNS_QUERY_REQUEST
 - PMDNS_QUERY_REQUEST
 - windns/PMDNS_QUERY_REQUEST
 - MDNS_QUERY_REQUEST
 - windns/MDNS_QUERY_REQUEST
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - _MDNS_QUERY_REQUEST
 - MDNS_QUERY_REQUEST
---

## -description

Contains the necessary information to perform an mDNS query.

## -struct-fields

### -field Version

The structure version must be **DNS_QUERY_REQUEST_VERSION1**.

### -field ulRefCount

Reserved. Do not use.

### -field Query

A string representing the name to be queried over mDNS.

### -field QueryType

A value representing the type of the records to be queried. See [DNS_RECORD_TYPE](/openspecs/windows_protocols/ms-dnsp/39b03b89-2264-4063-8198-d62f62a6441a) for possible values.

### -field QueryOptions

A value representing the query options. **DNS_QUERY_STANDARD** is the only supported value.

### -field InterfaceIndex

A value that contains the interface index over which the service is to be advertised. If `InterfaceIndex` is 0, then all interfaces will be considered.

### -field pQueryCallback

A pointer to a function (of type [MDNS_QUERY_CALLBACK](nc-windns-mdns_query_callback.md)) that represents the callback to be invoked asynchronously whenever mDNS results are available.

### -field pQueryContext

A pointer to a user context.

### -field fAnswerReceived

Reserved. Do not use.

### -field ulResendCount

Reserved. Do not use.

## -remarks

## -see-also