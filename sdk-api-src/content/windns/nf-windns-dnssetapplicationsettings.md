---
UID: NF:windns.DnsSetApplicationSettings
title: DnsSetApplicationSettings
description: Configures per-application DNS settings. This includes the ability to set per-application DNS servers either as fallback to the system configured servers, or exclusively.
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
 - DnsSetApplicationSettings
 - windns/DnsSetApplicationSettings
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
 - DnsSetApplicationSettings
prerelease: false
---

## -description

Configures per-application DNS settings. This includes the ability to set per-application DNS servers either as fallback to the system configured servers, or exclusively.

## -parameters

### -param cServers

Type: \_In\_ **[DWORD](/windows/win32/winprog/windows-data-types)**

The number of custom DNS servers present in the *pServers* parameter.

### -param pServers

Type: \_In\_reads\_(cServers) **[DNS_CUSTOM_SERVER](ns-windnsdef-dns_custom_server)\***

An array of [DNS_CUSTOM_SERVER](ns-windnsdef-dns_custom_server) that contains *cServers* elements. If *cServers* is 0, then this must be **NULL**.

### -param pSettings

Type: \_In\_opt\_ **[DNS_APPLICATION_SETTINGS](ns-windns-dns_application_settings.md)\***

A pointer to a [DNS_APPLICATION_SETTINGS](ns-windns-dns_application_settings.md) object describing additional settings for custom DNS servers.

If this is **NULL**, then the custom DNS servers passed to the API will be used as fallback to the system-configured ones.

If this points to a [DNS_APPLICATION_SETTINGS](ns-windns-dns_application_settings.md) object that has the **DNS_APP_SETTINGS_EXCLUSIVE_SERVERS** flag set in its *Flags* member, then it means use the custom DNS servers exclusively.

## -returns

A **DWORD** containing **ERROR_SUCCESS** on success, or an error code on failure.

## -remarks

## -see-also
