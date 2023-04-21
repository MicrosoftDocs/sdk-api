---
UID: NS:netioapi._DNS_INTERFACE_SETTINGS_EX
title: DNS_INTERFACE_SETTINGS_EX
description: Represents the DNS settings that can be configured on a given interface by calling the [**SetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings) function. (DNS_INTERFACE_SETTINGS_EX)
tech.root: IpHlp
ms.date: 07/15/2021
req.header: netioapi.h
req.construct-type: structure
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 19041
req.target-min-winversvr: Windows 10 Build 19041
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
req.typenames: DNS_INTERFACE_SETTINGS_EX
req.redist: 
f1_keywords:
 - _DNS_INTERFACE_SETTINGS_EX
 - netioapi/_DNS_INTERFACE_SETTINGS_EX
 - DNS_INTERFACE_SETTINGS_EX
 - netioapi/DNS_INTERFACE_SETTINGS_EX
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netioapi.h
api_name:
 - _DNS_INTERFACE_SETTINGS_EX
 - DNS_INTERFACE_SETTINGS_EX
---

## -description

Represents the DNS settings that can be configured on a given interface by calling the [**SetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings) function.

## -struct-fields

### -field SettingsV1

Type: **[DNS_INTERFACE_SETTINGS](ns-netioapi-dns_interface_settings.md)**

**SettingsV1::Version** must be set to **DNS_INTERFACE_SETTINGS_VERSION2**.

### -field SettingsV1::Flags

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

A bitmap of the following options.

**DNS_SETTING_IPV6** (0x0001). Configures the interface settings only for the IPv6 networking stack. If this option is set, then any IP addresses specified in the *NameServer* or *ProfileNameServer* members must be IPv6 addresses. By default, the DNS interface settings specified in this structure are applied only to the IPv4 networking stack.

**DNS_SETTING_NAMESERVER** (0x0002). Configures static adapter DNS servers on the specified interface via the *SettingsV1::NameServer* member.

**DNS_SETTING_SEARCHLIST** (0x0004). Configures the connection-specific DNS suffix search list for the given adapter via the *SettingsV1::SearchList* member.

**DNS_SETTING_REGISTRATION_ENABLED** (0x0008). Enables or disables the dynamic DNS registration for the given adapter. This is system-enabled by default.

**DNS_SETTING_DOMAIN** (0x0020). Configures the connection-specific DNS suffix for the given adapter via the *SettingsV1::Domain* member.

**DNS_SETTINGS_ENABLE_LLMNR** (0x0080). Enables or disables name resolution using LLMNR and mDNS on the specified adapter. This is system-enabled by default.

**DNS_SETTINGS_QUERY_ADAPTER_NAME** (0x0100). Enables or disables the use of the adapter name as a suffix for DNS queries. This is system-enabled by default.

**DNS_SETTING_PROFILE_NAMESERVER** (0x0200). Configures static profile DNS servers on the specified interface via the *SettingsV1::ProfileNameServer* member.

**DNS_SETTING_SUPPLEMENTAL_SEARCH_LIST** (0x0800). Configures the connection-specific DNS supplemental suffix search list for the given adapter via the *SupplementalSearchList* member.

### -field DisableUnconstrainedQueries

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

Reserved.

### -field SupplementalSearchList

Type: **[PWSTR](/windows/win32/winprog/windows-data-types)**

A NULL-terminated wide string containing a series of comma- or space-separated search names. For example, L"contoso1.com contoso2.com", or L"contoso1.com, contoso2.com".

## -remarks

## -see-also

* [GetInterfaceDnsSettings](/windows/win32/api/netioapi/nf-netioapi-getinterfacednssettings)
* [SetInterfaceDnsSettings](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings)
