---
UID: NE:windnsdef._DnsSection
title: DNS_SECTION (windnsdef.h)
description: The DNS_SECTION enumeration is used in record flags, and as an index into DNS wire message header section counts.
helpviewer_keywords: ["DNS_SECTION","DNS_SECTION enumeration [DNS]","DnsSectionAddtional","DnsSectionAnswer","DnsSectionAuthority","DnsSectionQuestion","dns.dns_section","windnsdef/DNS_SECTION","windnsdef/DnsSectionAddtional","windnsdef/DnsSectionAnswer","windnsdef/DnsSectionAuthority","windnsdef/DnsSectionQuestion"]
old-location: dns\dns_section.htm
tech.root: DNS
ms.assetid: d51ef2c7-c2bb-4eed-a026-a559460352b6
ms.date: 01/15/2025
ms.keywords: DNS_SECTION, DNS_SECTION enumeration [DNS], DnsSectionAddtional, DnsSectionAnswer, DnsSectionAuthority, DnsSectionQuestion, dns.dns_section, windnsdef/DNS_SECTION, windnsdef/DnsSectionAddtional, windnsdef/DnsSectionAnswer, windnsdef/DnsSectionAuthority, windnsdef/DnsSectionQuestion
req.header: windnsdef.h
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
req.typenames: DNS_SECTION
req.redist: 

f1_keywords:
 - _DnsSection
 - windnsdef/_DnsSection
 - DNS_SECTION
 - windnsdef/DNS_SECTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windnsdef.h
api_name:
 - DNS_SECTION
---

# DNS_SECTION enumeration


## -description

The <b>DNS_SECTION</b> enumeration is used in record flags, and as an index into DNS wire message header section counts.

## -enum-fields

### -field DnsSectionQuestion

The DNS section specified is a DNS question.

### -field DnsSectionAnswer

The DNS section specified is a DNS answer.

### -field DnsSectionAuthority

The DNS section specified indicates a DNS authority.

### -field DnsSectionAddtional

The DNS section specified is additional DNS information.

## -see-also

<a href="/windows/win32/DNS/dns-enumerations">DNS Enumerations</a>