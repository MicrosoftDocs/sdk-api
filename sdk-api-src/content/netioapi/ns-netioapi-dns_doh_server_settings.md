---
UID: NS:netioapi._DNS_DOH_SERVER_SETTINGS
title: DNS_DOH_SERVER_SETTINGS
description: Describes a DNS-over-HTTPS server.
tech.root: IpHlp
ms.date: 07/15/2021
req.header: netioapi.h
req.construct-type: structure
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DNS_DOH_SERVER_SETTINGS
req.redist: 
f1_keywords:
 - _DNS_DOH_SERVER_SETTINGS
 - netioapi/_DNS_DOH_SERVER_SETTINGS
 - DNS_DOH_SERVER_SETTINGS
 - netioapi/DNS_DOH_SERVER_SETTINGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netioapi.h
api_name:
 - _DNS_DOH_SERVER_SETTINGS
 - DNS_DOH_SERVER_SETTINGS
---

## -description

Describes a DNS-over-HTTPS server.

## -struct-fields

### -field Template

Type: **[PWSTR](/windows/win32/winprog/windows-data-types)**

A NULL-terminated wide string containing a valid DNS-over-HTTPS URI template.

This field must be NULL if the **DNS_DOH_SERVER_SETTINGS_ENABLE_AUTO** flag is present.

> [!IMPORTANT]
> The URI template mustn't contain an IP address as hostname that's different from the IP address of the referenced server. For example, if the referenced server is 1.1.1.1, and the URI template is `https://1.0.0.1/dns-query`, then that wouldn't be valid because 1.0.0.1 doesn't match the server IP 1.1.1.1.

### -field Flags

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

A bitmap containing any of the following options.

**DNS_DOH_SERVER_SETTINGS_ENABLE_AUTO** (0x0001). If this option is present, then the DNS server that's referenced by this property will load its URI template from the system DNS-over-HTTPS system list. When this option is present, the *Template* field must be set to NULL. This option must not be used together with the **DNS_DOH_SERVER_SETTINGS_ENABLE** option.

**DNS_DOH_SERVER_SETTINGS_ENABLE** (0x0002). If this option is present, then the *Template* field must point to a valid DNS-over-HTTPS URI template. This option must not be used together with the **DNS_DOH_SERVER_SETTINGS_ENABLE_AUTO** option.

**DNS_DOH_SERVER_SETTINGS_FALLBACK_TO_UDP** (0x0004). This option indicates that the referenced server may fallback to unsecure name resolution (UDP/TCP) if the DNS-over-HTTPS query failed. This option can be used only in addition to **DNS_DOH_SERVER_SETTINGS_ENABLE_AUTO** or **DNS_DOH_SERVER_SETTINGS_ENABLE**.

**DNS_DOH_AUTO_UPGRADE_SERVER** (0x0008). This option allows a DNS server present in an NRPT rule to use the DNS-over-HTTPS template if it has the same IP address as the server referenced by this property. This option can't be used by itself; it must be in addition to **DNS_DOH_SERVER_SETTINGS_ENABLE_AUTO** or **DNS_DOH_SERVER_SETTINGS_ENABLE**.

## -remarks

## -see-also
