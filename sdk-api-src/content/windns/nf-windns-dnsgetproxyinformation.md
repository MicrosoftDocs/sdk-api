---
UID: NF:windns.DnsGetProxyInformation
title: DnsGetProxyInformation function (windns.h)
description: The DnsGetProxyInformation function returns the proxy information for a DNS server's name resolution policy table.
helpviewer_keywords: ["DnsGetProxyInformation","DnsGetProxyInformation function [DNS]","dns.dnsgetproxyinformation","windns/DnsGetProxyInformation"]
old-location: dns\dnsgetproxyinformation.htm
tech.root: DNS
ms.assetid: fdc8eb09-e071-4f03-974a-2b11a657ab18
ms.date: 12/05/2018
ms.keywords: DnsGetProxyInformation, DnsGetProxyInformation function [DNS], dns.dnsgetproxyinformation, windns/DnsGetProxyInformation
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
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsGetProxyInformation
 - windns/DnsGetProxyInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsGetProxyInformation
---

# DnsGetProxyInformation function


## -description

The 
<b>DnsGetProxyInformation</b> function returns the proxy information for a DNS server's name resolution policy table.

## -parameters

### -param hostName [in]

A pointer to a string that represents the name of the DNS server whose proxy information is returned.

### -param proxyInformation [in, out]

A pointer to a <a href="/windows/desktop/api/windns/ns-windns-dns_proxy_information">DNS_PROXY_INFORMATION</a> structure that contains the proxy information for <i>hostName</i>.

### -param defaultProxyInformation [in, out, optional]

A pointer to a <a href="/windows/desktop/api/windns/ns-windns-dns_proxy_information">DNS_PROXY_INFORMATION</a> structure that contains the default proxy information for <i>hostName</i>. This proxy information is for the wildcard DNS policy.

### -param completionRoutine [in, optional]

Reserved. Do not use.

### -param completionContext [in, optional]

Reserved. Do not use.

## -returns

The 
<b>DnsGetProxyInformation</b> function returns the appropriate DNS-specific error code as defined in Winerror.h. The following are possible return values:

## -see-also

<a href="/windows/desktop/DNS/dns-functions">DNS Functions</a>