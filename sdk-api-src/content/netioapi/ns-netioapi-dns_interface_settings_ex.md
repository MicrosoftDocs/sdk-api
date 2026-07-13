---
UID: NS:netioapi._DNS_INTERFACE_SETTINGS_EX
title: DNS_INTERFACE_SETTINGS_EX
description: Represents the DNS settings that can be configured on a given interface by calling the [**SetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings) function or retrieved for a given interface by calling the [**GetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-getinterfacednssettings) function. (DNS_INTERFACE_SETTINGS_EX)
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

Represents the DNS settings that can be configured on a given interface by calling the [**SetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings) function or retrieved for a given interface by calling the [**GetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-getinterfacednssettings) function.

## -struct-fields

### -field SettingsV1

Type: **[DNS_INTERFACE_SETTINGS](ns-netioapi-dns_interface_settings.md)**

**SettingsV1.Version** must be set to **DNS_INTERFACE_SETTINGS_VERSION2**.

**SettingsV1.Flags** is configured in the same way as **[DNS_INTERFACE_SETTINGS::Flags](ns-netioapi-dns_interface_settings.md)**, with the additional following bitmap option:

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
