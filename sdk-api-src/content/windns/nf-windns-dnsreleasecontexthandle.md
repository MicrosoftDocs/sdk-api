---
UID: NF:windns.DnsReleaseContextHandle
title: DnsReleaseContextHandle function (windns.h)
description: The DnsReleaseContextHandle function releases memory used to store the credentials of a specific account.
helpviewer_keywords: ["DnsReleaseContextHandle","DnsReleaseContextHandle function [DNS]","_dns_dnsreleasecontexthandle","dns.dnsreleasecontexthandle","windns/DnsReleaseContextHandle"]
old-location: dns\dnsreleasecontexthandle.htm
tech.root: DNS
ms.assetid: 08a5fa73-4583-4e87-bddb-09bfbfe1b36f
ms.date: 12/05/2018
ms.keywords: DnsReleaseContextHandle, DnsReleaseContextHandle function [DNS], _dns_dnsreleasecontexthandle, dns.dnsreleasecontexthandle, windns/DnsReleaseContextHandle
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
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsReleaseContextHandle
 - windns/DnsReleaseContextHandle
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
 - DnsReleaseContextHandle
---

# DnsReleaseContextHandle function


## -description

The 
<b>DnsReleaseContextHandle</b> function releases memory used to store the credentials of a specific account.

## -parameters

### -param hContext [in]

The credentials handle of a specific account.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsacquirecontexthandle_a">DnsAcquireContextHandle</a>