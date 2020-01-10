---
UID: NE:windns.__unnamed_enum_1
title: DNS_FREE_TYPE (windns.h)
description: The DNS_FREE_TYPE enumeration specifies the type of data to free.
old-location: dns\dns_free_type.htm
tech.root: DNS
ms.assetid: 976982a1-08f1-4c67-b823-1eea34f0c643
ms.date: 12/05/2018
ms.keywords: DNS_FREE_TYPE, DNS_FREE_TYPE enumeration [DNS], DnsFreeFlat, DnsFreeParsedMessageFields, DnsFreeRecordList, dns.dns_free_type, windns/DNS_FREE_TYPE, windns/DnsFreeFlat, windns/DnsFreeParsedMessageFields, windns/DnsFreeRecordList
f1_keywords:
- windns/DNS_FREE_TYPE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Windns.h
api_name:
- DNS_FREE_TYPE
targetos: Windows
req.typenames: DNS_FREE_TYPE
req.redist: 
ms.custom: 19H1
---

# DNS_FREE_TYPE enumeration


## -description


The <b>DNS_FREE_TYPE</b> enumeration specifies the type of data to free.


## -enum-fields




### -field DnsFreeFlat

The data freed is a flat structure.


### -field DnsFreeRecordList

The data freed is a Resource Record list, and includes subfields of the <a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure. Resources freed include structures returned by the <a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a> and <a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsrecordsetcopyex">DnsRecordSetCopyEx</a> functions.


### -field DnsFreeParsedMessageFields

The data freed is a parsed message field.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DNS/dns-enumerations">DNS Enumerations</a>



<a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsqueryconfig">DnsQueryConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsrecordsetcopyex">DnsRecordSetCopyEx</a>
 

 

