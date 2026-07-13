---
UID: NS:netioapi._DNS_INTERFACE_SETTINGS
title: DNS_INTERFACE_SETTINGS
description: Represents the DNS settings that can be configured on a given interface by calling the [**SetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings) function or retrieved for a given interface by calling the [**GetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-getinterfacednssettings) function. (DNS_INTERFACE_SETTINGS)
tech.root: IpHlp
ms.date: 07/15/2021
req.header: netioapi.h
req.construct-type: structure
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 18362
req.target-min-winversvr: Windows 10 Build 18362
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
req.typenames: DNS_INTERFACE_SETTINGS
req.redist: 
f1_keywords:
 - _DNS_INTERFACE_SETTINGS
 - netioapi/_DNS_INTERFACE_SETTINGS
 - DNS_INTERFACE_SETTINGS
 - netioapi/DNS_INTERFACE_SETTINGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netioapi.h
api_name:
 - _DNS_INTERFACE_SETTINGS
 - DNS_INTERFACE_SETTINGS
---

## -description

Represents the DNS settings that can be configured on a given interface by calling the [**SetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings) function or retrieved for a given interface by calling the [**GetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-getinterfacednssettings) function.

## -struct-fields

### -field Version

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

Must be set to **DNS_INTERFACE_SETTINGS_VERSION1**.

### -field Flags

Type: **[ULONG64](/windows/win32/winprog/windows-data-types)**

A bitmap of the following options.
 
**DNS_SETTING_IPV6** (0x0001). Configures the interface settings only for the IPv6 networking stack. If this option is set, then any IP addresses specified in the *NameServer* or *ProfileNameServer* members must be IPv6 addresses. By default, the DNS interface settings specified in this structure are applied only to the IPv4 networking stack.

**DNS_SETTING_NAMESERVER** (0x0002). Configures static adapter DNS servers on the specified interface via the *NameServer* member.

**DNS_SETTING_SEARCHLIST** (0x0004). Configures the connection-specific DNS suffix search list for the given adapter via the *SearchList* member. 

**DNS_SETTING_REGISTRATION_ENABLED** (0x0008). Enables or disables the dynamic DNS registration for the given adapter. This is system-enabled by default.

**DNS_SETTING_DOMAIN** (0x0020). Configures the connection-specific DNS suffix for the given adapter via the *Domain* member.

**DNS_SETTINGS_ENABLE_LLMNR** (0x0080). Enables or disables name resolution using LLMNR and mDNS on the specified adapter. This is system-enabled by default.

**DNS_SETTINGS_QUERY_ADAPTER_NAME** (0x0100). Enables or disables the use of the adapter name as a suffix for DNS queries. This is system-enabled by default.

**DNS_SETTING_PROFILE_NAMESERVER** (0x0200). Configures static profile DNS servers on the specified interface via the *ProfileNameServer* member.

### -field Domain

Type: **[PWSTR](/windows/win32/winprog/windows-data-types)**

A NULL-terminated wide string containing the adapter domain name.

### -field NameServer

Type: **[PWSTR](/windows/win32/winprog/windows-data-types)**

A NULL-terminated wide string containing a series of comma- or space-separated DNS servers. For example, L"1.1.1.1 8.8.8.8", or L"1.1.1.1,8.8.8.8".
 
If the **DNS_SETTING_IPV6** flag is present, then the servers must be IPv6 addresses. For example, L"2606:4700:4700::1001,2606:4700:4700::1111".

### -field SearchList

Type: **[PWSTR](/windows/win32/winprog/windows-data-types)**

A NULL-terminated wide string containing a series of comma- or space-separated search names. For example, L"contoso1.com contoso2.com", or L"contoso1.com, contoso2.com".

### -field RegistrationEnabled

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

**TRUE** to enable adapter dynamic registration; **FALSE** to disable it.

### -field RegisterAdapterName

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

**TRUE** to enable adapter name registration; **FALSE** to disable it.

### -field EnableLLMNR

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

**TRUE** to enable mDNS and LLMNR on the given interface; **FALSE** to disable them.

### -field QueryAdapterName

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

**TRUE** if the adapter name should be used as a search suffix; otherwise **FALSE**.

### -field ProfileNameServer

Type: **[PWSTR](/windows/win32/winprog/windows-data-types)**

A NULL-terminated wide string containing a series of comma- or space-separated DNS servers. For example, L"1.1.1.1 8.8.8.8" or L"1.1.1.1,8.8.8.8".
 
If the **DNS_SETTING_IPV6** flag is present, then the servers must be IPv6 addresses. For example, L"2606:4700:4700::1001,2606:4700:4700::1111".

## -remarks

## -see-also

* [GetInterfaceDnsSettings](/windows/win32/api/netioapi/nf-netioapi-getinterfacednssettings)
* [SetInterfaceDnsSettings](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings)
