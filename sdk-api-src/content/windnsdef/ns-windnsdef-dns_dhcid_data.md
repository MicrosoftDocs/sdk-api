---
UID: NS:windnsdef.DNS_DHCID_DATA
title: DNS_DHCID_DATA (windnsdef.h)
description: Represents a DNS Dynamic Host Configuration Protocol Information (DHCID) resource record (RR) as specified in section 3 of RFC 4701.
helpviewer_keywords: ["*PDNS_DHCID_DATA","DNS_DHCID_DATA","DNS_DHCID_DATA structure [DNS]","PDNS_DHCID_DATA","PDNS_DHCID_DATA structure pointer [DNS]","dns.dns_dhcid_data","windnsdef/DNS_DHCID_DATA","windnsdef/PDNS_DHCID_DATA"]
old-location: dns\dns_dhcid_data.htm
tech.root: DNS
ms.assetid: 868846bc-9f63-4bb3-ac8d-cea34232bb41
ms.date: 01/15/2025
ms.keywords: '*PDNS_DHCID_DATA, DNS_DHCID_DATA, DNS_DHCID_DATA structure [DNS], PDNS_DHCID_DATA, PDNS_DHCID_DATA structure pointer [DNS], dns.dns_dhcid_data, windnsdef/DNS_DHCID_DATA, windnsdef/PDNS_DHCID_DATA'
req.header: windnsdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DNS_DHCID_DATA, *PDNS_DHCID_DATA
req.redist: 

f1_keywords:
 - PDNS_DHCID_DATA
 - windnsdef/PDNS_DHCID_DATA
 - DNS_DHCID_DATA
 - windnsdef/DNS_DHCID_DATA
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
 - DNS_DHCID_DATA
---

# DNS_DHCID_DATA structure


## -description

The <b>DNS_DHCID_DATA</b> structure represents a DNS Dynamic Host Configuration Protocol Information (DHCID) resource record (RR) as specified in section 3 of <a href="https://www.ietf.org/rfc/rfc4701.txt">RFC 4701</a>.

## -struct-fields

### -field dwByteCount

The length, in bytes, of <b>DHCID</b>.

### -field size_is

### -field size_is.dwByteCount

### -field DHCID

A <b>BYTE</b> array that contains the DHCID client, domain, and SHA-256 digest information as specified in section 4 of <a href="https://www.ietf.org/rfc/rfc2671.txt">RFC 2671</a>.

## -remarks

The 
<b>DNS_DHCID_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.

## -see-also

<a href="/windows/win32/DNS/dns-structures">DNS Structures</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

