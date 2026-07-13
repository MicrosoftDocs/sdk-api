---
UID: NS:windnsdef.DNS_LOC_DATA
title: DNS_LOC_DATA (windnsdef.h)
description: The DNS_LOC_DATA structure represents a DNS location (LOC) resource record (RR) as specified in RFC 1876.
helpviewer_keywords: ["*PDNS_LOC_DATA","DNS_LOC_DATA","DNS_LOC_DATA structure [DNS]","PDNS_LOC_DATA","PDNS_LOC_DATA structure pointer [DNS]","_dns_dns_loc_data","dns.dns_loc_data","windnsdef/DNS_LOC_DATA","windnsdef/PDNS_LOC_DATA"]
old-location: dns\dns_loc_data.htm
tech.root: DNS
ms.assetid: c1e05479-17f0-4993-8dcf-02036989d6dc
ms.date: 01/15/2025
ms.keywords: '*PDNS_LOC_DATA, DNS_LOC_DATA, DNS_LOC_DATA structure [DNS], PDNS_LOC_DATA, PDNS_LOC_DATA structure pointer [DNS], _dns_dns_loc_data, dns.dns_loc_data, windnsdef/DNS_LOC_DATA, windnsdef/PDNS_LOC_DATA'
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
req.typenames: DNS_LOC_DATA, *PDNS_LOC_DATA
req.redist: 

f1_keywords:
 - PDNS_LOC_DATA
 - windnsdef/PDNS_LOC_DATA
 - DNS_LOC_DATA
 - windnsdef/DNS_LOC_DATA
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
 - DNS_LOC_DATA
---

# DNS_LOC_DATA structure


## -description

The 
<b>DNS_LOC_DATA</b> structure represents a DNS location (LOC) resource record (RR) as specified in <a href="https://www.ietf.org/rfc/rfc1876.txt">RFC 1876</a>.

## -struct-fields

### -field wVersion

The version number of the representation. Must be zero.

### -field wSize

The diameter of a sphere enclosing the described entity, defined as "SIZE"         in section 2 of <a href="https://www.ietf.org/rfc/rfc1876.txt">RFC 1876</a>.

### -field wHorPrec

The horizontal data precision, defined as "HORIZ PRE"         in section 2 of <a href="https://www.ietf.org/rfc/rfc1876.txt">RFC 1876</a>.

### -field wVerPrec

The vertical data precision, defined as "VERT PRE"         in section 2 of <a href="https://www.ietf.org/rfc/rfc1876.txt">RFC 1876</a>.

### -field dwLatitude

The latitude of the center of the sphere, defined as "LATITUDE"         in section 2 of <a href="https://www.ietf.org/rfc/rfc1876.txt">RFC 1876</a>.

### -field dwLongitude

The longitude of the center of the sphere, defined as "LONGITUDE"         in section 2 of <a href="https://www.ietf.org/rfc/rfc1876.txt">RFC 1876</a>.

### -field dwAltitude

The altitude of the center of the sphere, defined as "ALTITUDE"         in section 2 of <a href="https://www.ietf.org/rfc/rfc1876.txt">RFC 1876</a>.

## -remarks

The 
<b>DNS_LOC_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

