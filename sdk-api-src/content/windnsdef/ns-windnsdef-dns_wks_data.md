---
UID: NS:windnsdef.DNS_WKS_DATA
title: DNS_WKS_DATA (windnsdef.h)
description: The DNS_WKS_DATA structure represents a DNS well-known services (WKS) record as specified in section 3.4.2 of RFC 1035.
helpviewer_keywords: ["*PDNS_WKS_DATA","DNS_WKS_DATA","DNS_WKS_DATA structure [DNS]","PDNS_WKS_DATA","PDNS_WKS_DATA structure pointer [DNS]","Transmission Control Protocol (TCP)","User Datagram Protocol (UDP)","_dns_dns_wks_data","dns.dns_wks_data","windnsdef/DNS_WKS_DATA","windnsdef/PDNS_WKS_DATA"]
old-location: dns\dns_wks_data.htm
tech.root: DNS
ms.assetid: 94477345-74e7-40bf-a75b-e4bf67f1c17b
ms.date: 01/15/2025
ms.keywords: '*PDNS_WKS_DATA, DNS_WKS_DATA, DNS_WKS_DATA structure [DNS], PDNS_WKS_DATA, PDNS_WKS_DATA structure pointer [DNS], Transmission Control Protocol (TCP), User Datagram Protocol (UDP), _dns_dns_wks_data, dns.dns_wks_data, windnsdef/DNS_WKS_DATA, windnsdef/PDNS_WKS_DATA'
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
req.typenames: DNS_WKS_DATA, *PDNS_WKS_DATA
req.redist: 

f1_keywords:
 - PDNS_WKS_DATA
 - windnsdef/PDNS_WKS_DATA
 - DNS_WKS_DATA
 - windnsdef/DNS_WKS_DATA
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
 - DNS_WKS_DATA
---

# DNS_WKS_DATA structure


## -description

The 
<b>DNS_WKS_DATA</b> structure represents a DNS well-known services (WKS) record as specified in section 3.4.2 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>.

## -struct-fields

### -field IpAddress

An <a href="/windows/win32/DNS/dns-data-types">IP4_ADDRESS</a> data type that contains the IPv4 address for this resource record (RR).

### -field chProtocol

A value that represents the IP protocol for this RR as defined in <a href="https://www.ietf.org/rfc/rfc1010.txt">RFC 1010</a>.



#### Transmission Control Protocol (TCP) (6)



#### User Datagram Protocol (UDP) (17)

### -field BitMask

A variable-length bitmask whose bits correspond to the port number of well known services offered by the protocol specified in <b>chProtocol</b>. The bitmask has one bit for every port of the supported protocol, but must be a multiple of a <b>BYTE</b>. Bit 0 corresponds to port 1, bit 1 corresponds to port 2, and so forth for a maximum of 1024 bits.

## -remarks

The 
<b>DNS_WKS_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

