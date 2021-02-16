---
UID: NE:windns._DNS_NAME_FORMAT
title: DNS_NAME_FORMAT (windns.h)
description: The DNS_NAME_FORMAT enumeration specifies name format information for DNS.
helpviewer_keywords: ["DNS_NAME_FORMAT","DNS_NAME_FORMAT enumeration [DNS]","DnsNameDomain","DnsNameDomainLabel","DnsNameHostnameFull","DnsNameHostnameLabel","DnsNameSrvRecord","DnsNameValidateTld","DnsNameWildcard","dns.dns_name_format","windns/DNS_NAME_FORMAT","windns/DnsNameDomain","windns/DnsNameDomainLabel","windns/DnsNameHostnameFull","windns/DnsNameHostnameLabel","windns/DnsNameSrvRecord","windns/DnsNameValidateTld","windns/DnsNameWildcard"]
old-location: dns\dns_name_format.htm
tech.root: DNS
ms.assetid: f6f1cff3-4bff-4a07-bbc6-5255030b4164
ms.date: 12/05/2018
ms.keywords: DNS_NAME_FORMAT, DNS_NAME_FORMAT enumeration [DNS], DnsNameDomain, DnsNameDomainLabel, DnsNameHostnameFull, DnsNameHostnameLabel, DnsNameSrvRecord, DnsNameValidateTld, DnsNameWildcard, dns.dns_name_format, windns/DNS_NAME_FORMAT, windns/DnsNameDomain, windns/DnsNameDomainLabel, windns/DnsNameHostnameFull, windns/DnsNameHostnameLabel, windns/DnsNameSrvRecord, windns/DnsNameValidateTld, windns/DnsNameWildcard
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DNS_NAME_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DNS_NAME_FORMAT
 - windns/_DNS_NAME_FORMAT
 - DNS_NAME_FORMAT
 - windns/DNS_NAME_FORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_NAME_FORMAT
---

# DNS_NAME_FORMAT enumeration


## -description

The <b>DNS_NAME_FORMAT</b> enumeration specifies name format information for DNS.

## -enum-fields

### -field DnsNameDomain

The name format is a DNS domain.

### -field DnsNameDomainLabel

The name format is a DNS domain label.

### -field DnsNameHostnameFull

The name format is a full DNS host name.

### -field DnsNameHostnameLabel

The name format is a  DNS host label.

### -field DnsNameWildcard

The name format is a  DNS wildcard.

### -field DnsNameSrvRecord

The name format is a  DNS SRV record.

### -field DnsNameValidateTld

Windows 7 or later: The name format is a DNS domain or a full DNS host name.

## -see-also

<a href="/windows/desktop/DNS/dns-enumerations">DNS Enumerations</a>