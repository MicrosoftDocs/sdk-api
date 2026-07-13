---
UID: NF:windns.DnsGetApplicationSettings
title: DnsGetApplicationSettings
description: Retrieves the per-application DNS settings.
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
 - DnsGetApplicationSettings
 - windns/DnsGetApplicationSettings
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
 - DnsGetApplicationSettings
prerelease: false
---

## -description

Retrieves the per-application DNS settings.

## -parameters

### -param pcServers

Type: \_Out\_ **[DWORD](/windows/win32/winprog/windows-data-types)\***

After the function call, this will point to the number of custom DNS servers that the application has configured. If there are no custom servers configured, or if the function fails, then this will be set to 0.

### -param ppDefaultServers

Type: \_Outptr\_result\_buffer\_(*pcServers) **[DNS_CUSTOM_SERVER](ns-windnsdef-dns_custom_server)\*\***

After the function call, this will point to the array of DNS custom servers that are configured for the application. If the application has no servers configured, or if the function fails, then this will be set to **NULL**.

### -param pSettings

Type: \_Out\_opt\_ **[DNS_APPLICATION_SETTINGS](ns-windns-dns_application_settings.md)\***

A pointer to a [DNS_APPLICATION_SETTINGS](ns-windns-dns_application_settings.md) object, populated with the application settings.

## -returns

A **DWORD** containing **ERROR_SUCCESS** on success, or an error code on failure.

## -remarks

To avoid memory leaks, you must call [DnsFreeCustomServers](nf-windns-dnsfreecustomservers.md) on the servers returned by **DnsGetApplicationSettings** via its *pSettings* parameter.

## -see-also

* [DnsFreeCustomServers](nf-windns-dnsfreecustomservers.md)
