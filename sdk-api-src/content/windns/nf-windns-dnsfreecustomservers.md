---
UID: NF:windns.DnsFreeCustomServers
title: DnsFreeCustomServers
description: Frees the array of custom servers that was returned from a previous call to [DnsGetApplicationSettings](/windows/win32/api/windns/nf-windns-dnsgetapplicationsettings).
tech.root: DNS
ms.date: 09/01/2021
req.construct-type: function
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
f1_keywords:
 - DnsFreeCustomServers
 - windns/DnsFreeCustomServers
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
 - DnsFreeCustomServers
prerelease: false
---

## -description

Frees the array of custom servers that was returned from a previous call to [DnsGetApplicationSettings](/windows/win32/api/windns/nf-windns-dnsgetapplicationsettings).

## -parameters

### -param pcServers

Type: \_Inout\_ **[DWORD](/windows/win32/winprog/windows-data-types)\***

A pointer to a **DWORD** that contains the number of servers present in the array pointed to by *ppServers*. This will be set to 0 after the function call.

### -param ppServers

Type: \_Inout\_ **[DNS_CUSTOM_SERVER](ns-windnsdef-dns_custom_server)\*\***

A pointer to an array of [DNS_CUSTOM_SERVER](ns-windnsdef-dns_custom_server) that contains *pcServers* elements. This will be set to **NULL** after the function call.

## -remarks

To avoid memory leaks, you must call **DnsFreeCustomServers** on the servers returned by [DnsGetApplicationSettings](nf-windns-dnsgetapplicationsettings.md) via its *pSettings* parameter.

## -see-also

* [DnsGetApplicationSettings](nf-windns-dnsgetapplicationsettings.md)
