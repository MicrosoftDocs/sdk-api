---
UID: NS:windns.DNS_PROXY_INFORMATION
title: DNS_PROXY_INFORMATION (windns.h)
description: Contains the proxy information for a DNS server's name resolution policy table.
helpviewer_keywords: ["DNS_PROXY_INFORMATION","DNS_PROXY_INFORMATION structure [DNS]","PDNS_PROXY_INFORMATION","PDNS_PROXY_INFORMATION structure pointer [DNS]","dns.dns_proxy_information","windns/DNS_PROXY_INFORMATION","windns/PDNS_PROXY_INFORMATION"]
old-location: dns\dns_proxy_information.htm
tech.root: DNS
ms.assetid: cfe7653f-7e68-4e50-ba67-bd441f837ef8
ms.date: 12/05/2018
ms.keywords: DNS_PROXY_INFORMATION, DNS_PROXY_INFORMATION structure [DNS], PDNS_PROXY_INFORMATION, PDNS_PROXY_INFORMATION structure pointer [DNS], dns.dns_proxy_information, windns/DNS_PROXY_INFORMATION, windns/PDNS_PROXY_INFORMATION
req.header: windns.h
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
req.typenames: DNS_PROXY_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DNS_PROXY_INFORMATION
 - windns/DNS_PROXY_INFORMATION
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
 - DNS_PROXY_INFORMATION
---

# DNS_PROXY_INFORMATION structure


## -description

The <b>DNS_PROXY_INFORMATION</b> structure  contains the proxy information for a DNS server's name resolution policy table.

## -struct-fields

### -field version

A value that specifies the structure version. This value must be 1.

### -field proxyInformationType

A <a href="/windows/desktop/api/windns/ne-windns-dns_proxy_information_type">DNS_PROXY_INFORMATION_TYPE</a> enumeration that contains the proxy information type.

### -field proxyName

A pointer to a string that contains the proxy server name if <b>proxyInformationType</b> is <b>DNS_PROXY_INFORMATION_PROXY_NAME</b>. Otherwise, this member is ignored.

<div class="alert"><b>Note</b>  To free this string, use the 
<a href="/windows/desktop/api/windns/nf-windns-dnsfreeproxyname">DnsFreeProxyName</a> function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/DNS/dns-structures">DNS Structures</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsgetproxyinformation">DnsGetProxyInformation</a>