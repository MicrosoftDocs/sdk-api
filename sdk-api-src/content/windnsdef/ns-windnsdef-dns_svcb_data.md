---
UID: NS:windnsdef._DNS_SVCB_DATA
title: DNS_SVCB_DATA
description: The DNS_SVCB_DATA structure represents a DNS SVCB ("Service Binding") record, as specified in RFC 9460.
tech.root: DNS
ms.date: 07/03/2025
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: windnsdef.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: DNS_SVCB_DATA
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windnsdef.h
api_name:
 - _DNS_SVCB_DATA
 - DNS_SVCB_DATA
f1_keywords:
 - _DNS_SVCB_DATA
 - windnsdef/_DNS_SVCB_DATA
 - DNS_SVCB_DATA
 - windnsdef/DNS_SVCB_DATA
dev_langs:
 - c++
helpviewer_keywords:
 - _DNS_SVCB_DATA
---

## -description

The **DNS_SVCB_DATA** structure represents a DNS SVCB ("Service Binding") record, as specified in RFC 9460.

## -struct-fields

### -field wSvcPriority

Type: **[WORD](/windows/win32/winprog/windows-data-types)**

Record priority. A lower value indicates higher priority; 0 indicates Alias Mode, as described in section 2.4.2 of RFC 9460.

### -field pszTargetName

Type: **[PSTR](/windows/win32/winprog/windows-data-types)**

A pointer to a null-terminated string representing the domain name of the target or alternative endpoint.

### -field cSvcParams

Type: **[WORD](/windows/win32/winprog/windows-data-types)**

Count of svcb parameters.

### -field pSvcParams

Type: **[DNS_SVCB_PARAM](./ns-windnsdef-dns_svcb_param.md)\***

List of SVCB parameters representing the services available at *pszTargetName*.

## -remarks

When calling [DnsQueryEx](/windows/win32/api/windns/nf-windns-dnsqueryex) (or any of the DNS query APIs) for [**DNS_TYPE_SVCB**](/windows/win32/dns/dns-constants#dns-record-types) or **DNS_TYPE_HTTPS** DNS record types, if you want to get back results in a parsed format&mdash;that is, in the form of a **DNS_SVCB_DATA** structure instead of a 'flat' (just a data buffer) format&mdash;then you must set DNS_QUERY_PARSE_ALL_RECORDS (in [DNS_QUERY_REQUEST3::QueryOptions](/windows/win32/api/windns/ns-windns-dns_query_request3)).

## -see-also
