---
UID: NS:netioapi._DNS_SERVER_PROPERTY
title: DNS_SERVER_PROPERTY
description: Describes a DNS server property, which is set in the [**DNS_INTERFACE_SETTINGS3**](/windows/win32/api/netioapi/ns-netioapi-dns_interface_settings3) structure, and configured through the [**SetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings) function.
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
req.typenames: DNS_SERVER_PROPERTY
req.redist: 
f1_keywords:
 - _DNS_SERVER_PROPERTY
 - netioapi/_DNS_SERVER_PROPERTY
 - DNS_SERVER_PROPERTY
 - netioapi/DNS_SERVER_PROPERTY
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netioapi.h
api_name:
 - _DNS_SERVER_PROPERTY
 - DNS_SERVER_PROPERTY
---

## -description

Describes a DNS server property, which is set in the [**DNS_INTERFACE_SETTINGS3**](/windows/win32/api/netioapi/ns-netioapi-dns_interface_settings3) structure, and configured through the [**SetInterfaceDnsSettings**](/windows/win32/api/netioapi/nf-netioapi-setinterfacednssettings) function.

## -struct-fields

### -field Version

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

Must be set to **DNS_INTERFACE_SETTINGS_VERSION1**.

### -field ServerIndex

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

Must be the index of the corresponding server present in the [**DNS_INTERFACE_SETTINGS3::NameServer**](/windows/win32/api/netioapi/ns-netioapi-dns_interface_settings3) or **::ProfileNameServer** member. For proper usage, see the *ServerProperties* and *ProfileServerProperties* members in the topic for the [**DNS_INTERFACE_SETTINGS3**](ns-netioapi-dns_interface_settings3.md) structure.

### -field Type

Type: **[DNS_SERVER_PROPERTY_TYPE](ne-netioapi-dns_server_property_type.md)**

Must be set to **DnsServerDohProperty**. Describes a DNS-over-HTTPS server property.

### -field Property

Type: **[DNS_SERVER_PROPERTY_TYPES](ns-netioapi-dns_server_property_types.md)**

If the *Type* member is set to **DnsServerDohProperty**, then the **DNS_SERVER_PROPERTY_TYPES::DohSettings** field must point to a valid **DNS_DOH_SERVER_SETTINGS** object.

## -remarks

## -see-also
