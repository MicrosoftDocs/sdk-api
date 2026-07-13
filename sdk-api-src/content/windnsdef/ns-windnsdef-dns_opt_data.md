---
UID: NS:windnsdef.DNS_OPT_DATA
title: DNS_OPT_DATA (windnsdef.h)
description: Represents a DNS Option (OPT) resource record (RR) as specified in section 4 of RFC 2671.
helpviewer_keywords: ["*PDNS_OPT_DATA","DNS_OPT_DATA","DNS_OPT_DATA structure [DNS]","PDNS_OPT_DATA","PDNS_OPT_DATA structure pointer [DNS]","dns.dns_opt_data","windnsdef/DNS_OPT_DATA","windnsdef/PDNS_OPT_DATA"]
old-location: dns\dns_opt_data.htm
tech.root: DNS
ms.assetid: a8e23127-a625-4206-abe8-0787b4ac0f30
ms.date: 01/15/2025
ms.keywords: '*PDNS_OPT_DATA, DNS_OPT_DATA, DNS_OPT_DATA structure [DNS], PDNS_OPT_DATA, PDNS_OPT_DATA structure pointer [DNS], dns.dns_opt_data, windnsdef/DNS_OPT_DATA, windnsdef/PDNS_OPT_DATA'
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
req.typenames: DNS_OPT_DATA, *PDNS_OPT_DATA
req.redist: 

f1_keywords:
 - PDNS_OPT_DATA
 - windnsdef/PDNS_OPT_DATA
 - DNS_OPT_DATA
 - windnsdef/DNS_OPT_DATA
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
 - DNS_OPT_DATA
---

# DNS_OPT_DATA structure


## -description

The <b>DNS_OPT_DATA</b> structure represents a DNS Option  (OPT) resource record (RR) as specified in section 4 of <a href="https://www.ietf.org/rfc/rfc2671.txt">RFC 2671</a>.

## -struct-fields

### -field wDataLength

The length, in bytes, of <b>Data</b>.

### -field wPad

Reserved. Do not use.

### -field size_is

### -field size_is.wDataLength

### -field Data

A <b>BYTE</b> array that contains variable transport level information as specified in section 4 of <a href="https://www.ietf.org/rfc/rfc2671.txt">RFC 2671</a>.

## -remarks

The 
<b>DNS_OPT_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.

## -see-also

<a href="/windows/win32/DNS/dns-structures">DNS Structures</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

