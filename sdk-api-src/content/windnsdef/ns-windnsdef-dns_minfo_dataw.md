---
UID: NS:windnsdef.DNS_MINFO_DATAW
title: DNS_MINFO_DATAW (windnsdef.h)
description: The DNS_MINFO_DATA structure represents a DNS mail information (MINFO) record as specified in section 3.3.7 of RFC 1035. (Unicode)
helpviewer_keywords: ["*PDNS_MINFO_DATA","*PDNS_MINFO_DATAW","DNS_MINFO_DATA","DNS_MINFO_DATA structure [DNS]","DNS_MINFO_DATAW","PDNS_MINFO_DATA","PDNS_MINFO_DATA structure pointer [DNS]","_dns_dns_minfo_data","dns.dns_minfo_data","windnsdef/DNS_MINFO_DATA","windnsdef/PDNS_MINFO_DATA"]
old-location: dns\dns_minfo_data.htm
tech.root: DNS
ms.assetid: cd392b48-734f-462b-b893-855f07c30575
ms.date: 01/15/2025
ms.keywords: '*PDNS_MINFO_DATA, *PDNS_MINFO_DATAW, DNS_MINFO_DATA, DNS_MINFO_DATA structure [DNS], DNS_MINFO_DATAW, PDNS_MINFO_DATA, PDNS_MINFO_DATA structure pointer [DNS], _dns_dns_minfo_data, dns.dns_minfo_data, windnsdef/DNS_MINFO_DATA, windnsdef/PDNS_MINFO_DATA'
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
req.typenames: DNS_MINFO_DATAW, *PDNS_MINFO_DATAW
req.redist: 

f1_keywords:
 - PDNS_MINFO_DATAW
 - windnsdef/PDNS_MINFO_DATAW
 - DNS_MINFO_DATAW
 - windnsdef/DNS_MINFO_DATAW
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
 - DNS_MINFO_DATA
---

# DNS_MINFO_DATAW structure


## -description

The 
<b>DNS_MINFO_DATA</b> structure represents a DNS mail information (MINFO) record as specified in section 3.3.7 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>.

## -struct-fields

### -field pNameMailbox

A pointer to a string that represents the <a href="/windows/win32/dns/f-gly">fully qualified domain name</a> (FQDN) of the mailbox responsible for the mailing list or mailbox specified in the record's owner name.

### -field pNameErrorsMailbox

A pointer to a string that represents the FQDN of the mailbox to receive error messages related to the mailing list.

## -remarks

The 
<b>DNS_MINFO_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.





> [!NOTE]
> The windns.h header defines DNS_MINFO_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

