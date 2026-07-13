---
UID: NS:windns._DNS_QUERY_RAW_RESULT
title: DNS_QUERY_RAW_RESULT
description: Represents a DNS raw query result (see [DNS_QUERY_RAW_COMPLETION_ROUTINE](./nc-windns-dns_query_raw_completion_routine.md)).
tech.root: DNS
ms.date: 07/17/2023
targetos: Windows
prerelease: true
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: windns.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.typenames: DNS_QUERY_RAW_RESULT
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - _DNS_QUERY_RAW_RESULT
 - DNS_QUERY_RAW_RESULT
f1_keywords:
 - _DNS_QUERY_RAW_RESULT
 - windns/_DNS_QUERY_RAW_RESULT
 - DNS_QUERY_RAW_RESULT
 - windns/DNS_QUERY_RAW_RESULT
dev_langs:
 - c++
helpviewer_keywords:
 - _DNS_QUERY_RAW_RESULT
---

## -description

Represents a DNS raw query result (see [DNS_QUERY_RAW_COMPLETION_ROUTINE](./nc-windns-dns_query_raw_completion_routine.md)).

## -struct-fields

### -field version

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

The version of this structure. This matches what was set in [DNS_QUERY_RAW_REQUEST::resultsVersion](./ns-windns-dns_query_raw_request.md). Currently only **DNS_QUERY_RAW_RESULT_VERSION1** (0x1) exists.

### -field queryStatus

Type: **DNS_STATUS**

The status of the query.

### -field queryOptions

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

Query options that were used in this query. Due to system configuration, these might be different from the query options that you provided in the request. The current options are defined in [DNS query options](/windows/win32/dns/dns-constants#dns-query-options).

### -field queryRawOptions

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

Additional options that were applied to the raw query. Also see [DNS_QUERY_RAW_REQUEST::queryRawOptions](./ns-windns-dns_query_raw_request.md).

### -field responseFlags

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

Additional flags about the query response. Currently none are specified.

### -field queryRawResponseSize

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

Count of bytes in the DNS raw response buffer pointed to by *queryRawResponse*.

### -field queryRawResponse

Type: **[BYTE](/windows/win32/winprog/windows-data-types)\***

Pointer to a buffer containing the wire representation of the DNS query response&mdash;a 12-byte header followed by a variable number of records. This buffer is of size *queryRawResponseSize* bytes.

The pointer might or might not be valid depending on *queryStatus*. Internal DNS errors would produce an error status and a `NULL` pointer, but negative responses from the server could produce error status and a valid pointer. If the queryStatus is **ERROR_SUCCESS**, then the pointer is valid.

### -field queryRecords

Type: **PDNS_RECORD**

Pointer to a [DNS_RECORD](/windows/win32/api/windnsdef/ns-windnsdef-dns_recordw) structure. This contains the same records as in *queryRawResponse*, but parsed out into a structure format.

This pointer is valid in the same ways as *queryRawResponse*, where it's dependent on the *queryStatus* value.

*queryRecords* contains the same records as in *queryRawResponse*, but parsed out into a structure format. However, if there's a new type of DNS record in the response that's not known by the implementation, then that won't be present in *queryRecords*; but it will be present in *queryRawResponse*.

### -field protocol

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

The DNS protocol used for the query response. This doesn't necessarily match the protocol in [DNS_QUERY_RAW_REQUEST](./ns-windns-dns_query_raw_request.md) because the DNS system might have changed the outgoing query protocol based on configuration. The query response will be modified, if needed, to match the protocol in the request so that the behavior seen by the caller is seamless. A value of **DNS_PROTOCOL_NO_WIRE** indicates that the result records and data were produced internally and the DNS system didn't send a query on the wire.

Possible values include:

* **DNS_PROTOCOL_UNSPECIFIED** (0x0). The query completed without receiving a response; such as in a cancellation.
* **DNS_PROTOCOL_UDP** (0x1).
* **DNS_PROTOCOL_TCP** (0x2).
* **DNS_PROTOCOL_DOH** (0x3).
* **DNS_PROTOCOL_DOT** (0x4).
* **DNS_PROTOCOL_NO_WIRE** (0x5). The query completed inline; such as with records from the cache.

### -field sourceAddr

Type: **[SOCKADDR_INET](/windows/win32/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet)**

The address of the source of the DNS raw response.

### -field maxSa

Type: **[CHAR](/windows/win32/winprog/windows-data-types)\[\]**

The address of the source of the DNS raw response. You can use the *maxSa* array in code that doesn't have the [SOCKADDR_INET](/windows/win32/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet) type defined.

## -remarks

## -see-also
