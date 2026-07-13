---
UID: NS:windns._DNS_QUERY_REQUEST3
title: DNS_QUERY_REQUEST3
description: Contains the DNS query parameters used in a call to [DnsQueryEx](/windows/win32/api/windns/nf-windns-dnsqueryex).
tech.root: DNS
ms.date: 05/28/2021
prerelease: false
req.construct-type: structure
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DNS_QUERY_REQUEST3, *PDNS_QUERY_REQUEST3
req.redist: 
f1_keywords:
 - _DNS_QUERY_REQUEST3
 - windns/_DNS_QUERY_REQUEST3
 - PDNS_QUERY_REQUEST3
 - windns/PDNS_QUERY_REQUEST3
 - DNS_QUERY_REQUEST3
 - windns/DNS_QUERY_REQUEST3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - _DNS_QUERY_REQUEST3
 - PDNS_QUERY_REQUEST3
 - DNS_QUERY_REQUEST3
---

## -description

Contains the DNS query parameters used in a call to [DnsQueryEx](/windows/win32/api/windns/nf-windns-dnsqueryex).

## -struct-fields

### -field Version

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

The structure version must be the **DNS_QUERY_REQUEST_VERSION3**; which has a value of 3.

### -field QueryName

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

A pointer to a string that represents the DNS name to query.

> [!NOTE]
> If *QueryName* is **NULL**, then the query is for the local machine name.

### -field QueryType

Type: **[WORD](/windows/win32/winprog/windows-data-types)**

A value that represents the Resource Record (RR) [DNS Record Type](/windows/win32/dns/dns-constants#dns-record-types) that is queried. *QueryType* determines the format of data pointed to by *pQueryRecords* returned in the [DNS_QUERY_RESULT](/windows/win32/api/windns/ns-windns-dns_query_result) structure. For example, if the value of *wType* is [DNS_TYPE_A](/windows/win32/dns/dns-constants), then the format of data pointed to by *pQueryRecords* is [DNS_A_DATA](/windows/win32/api/windnsdef/ns-windnsdef-dns_a_data).

### -field QueryOptions

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

A value that contains a bitmap of [DNS Query Options](/windows/win32/dns/dns-constants#dns-query-options) to use in the DNS query. Options can be combined, and all options override **DNS_QUERY_STANDARD**.

### -field pDnsServerList

Type: **[PDNS_ADDR_ARRAY](/windows/win32/api/windnsdef/ns-windnsdef-dns_addr_array)**

A pointer to a [DNS_ADDR_ARRAY](/windows/win32/api/windnsdef/ns-windnsdef-dns_addr_array) structure that contains a list of DNS servers to use in the query.

### -field InterfaceIndex

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

A value that contains the interface index over which the query is sent. If *InterfaceIndex* is 0, then all interfaces will be considered.

### -field pQueryCompletionCallback

Type: **[PDNS_QUERY_COMPLETION_ROUTINE](/windows/win32/api/windns/nc-windns-dns_query_completion_routine)**

A pointer to a [DNS_QUERY_COMPLETION_ROUTINE](/windows/win32/api/windns/nc-windns-dns_query_completion_routine) callback that is used to return the results of an asynchronous query from a call to [DnsQueryEx](/windows/win32/api/windns/nf-windns-dnsqueryex).

> [!NOTE]
> If **NULL**, then [DnsQueryEx](/windows/win32/api/windns/nf-windns-dnsqueryex) is called synchronously.

### -field pQueryContext

Type: **[PVOID](/windows/win32/winprog/windows-data-types)**

A pointer to a user context.

### -field IsNetworkQueryRequired

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

Reserved.

### -field RequiredNetworkIndex

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

Reserved.

### -field cCustomServers

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

The number of custom servers pointed to by the *pCustomServers* member.

### -field pCustomServers

Type: \_Field\_size\_(cCustomServers) **[DNS_CUSTOM_SERVER](/windows/win32/api/windnsdef/ns-windnsdef-dns_custom_server)\***

A pointer to an array of N (where N is given in the *cCustomServers* field) [DNS_CUSTOM_SERVER](/windows/win32/api/windnsdef/ns-windnsdef-dns_custom_server) objects.

If *cCustomServers* is 0, then *pCustomServers* must be **NULL**.

> [!NOTE]
> At least one of *pCustomServers* and *pDnsServerList* must be **NULL**. Both set to non-**NULL** values at the same time is not supported.

## -remarks

The custom servers specified in *pCustomServers* bypass the system-configured DNS servers.

If the query name matches a rule in the **Name Resolution Policy Table (NRPT)**, then the custom servers are ignored, and only the servers from the **NRPT** rule are used.

## -see-also

* [DNS_ADDR_ARRAY](/windows/win32/api/windnsdef/ns-windnsdef-dns_addr_array)
* [DNS constants](/windows/win32/dns/dns-constants)
* [DNS_CUSTOM_SERVER](/windows/win32/api/windnsdef/ns-windnsdef-dns_custom_server)
* [DnsQueryEx function](/windows/win32/api/windns/nf-windns-dnsqueryex)
* [DNS_QUERY_RESULT](/windows/win32/api/windns/ns-windns-dns_query_result)
