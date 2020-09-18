---
UID: NF:windns.DnsFreeProxyName
title: DnsFreeProxyName function (windns.h)
description: Frees memory allocated for the proxyName member of a DNS_PROXY_INFORMATION structure obtained using the DnsGetProxyInformation function.
helpviewer_keywords: ["DnsFreeProxyName","DnsFreeProxyName function [DNS]","dns.dnsfreeproxyname","windns/DnsFreeProxyName"]
old-location: dns\dnsfreeproxyname.htm
tech.root: DNS
ms.assetid: 4c69d548-3bb5-4609-9fc5-3a829a285956
ms.date: 12/05/2018
ms.keywords: DnsFreeProxyName, DnsFreeProxyName function [DNS], dns.dnsfreeproxyname, windns/DnsFreeProxyName
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
 - DnsFreeProxyName
 - windns/DnsFreeProxyName
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
 - DnsFreeProxyName
---

# DnsFreeProxyName function


## -description

The 
<b>DnsFreeProxyName</b> function frees memory allocated for the <b>proxyName</b> member of a <a href="/windows/desktop/api/windns/ns-windns-dns_proxy_information">DNS_PROXY_INFORMATION</a> structure obtained using the 
<a href="/windows/desktop/api/windns/nf-windns-dnsgetproxyinformation">DnsGetProxyInformation</a> function.

## -parameters

### -param proxyName [in, out]

A pointer to the <b>proxyName</b> string to be freed.

## -see-also

<a href="/windows/desktop/DNS/dns-functions">DNS Functions</a>