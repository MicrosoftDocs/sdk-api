---
UID: NE:netioapi._DNS_SERVER_PROPERTY_TYPE
title: DNS_SERVER_PROPERTY_TYPE
description: Defines constants that specify the validity of the property held in the [DNS_SERVER_PROPERTY::Property](ns-netioapi-dns_server_property.md) member.
tech.root: IpHlp
ms.date: 07/16/2021
req.construct-type: enumeration
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: MIB_IF_TABLE_LEVEL, *PMIB_IF_TABLE_LEVEL
req.redist: 
f1_keywords:
 - _DNS_SERVER_PROPERTY_TYPE
 - netioapi/_DNS_SERVER_PROPERTY_TYPE
 - DNS_SERVER_PROPERTY_TYPE
 - netioapi/DNS_SERVER_PROPERTY_TYPE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netioapi.h
api_name:
 - _DNS_SERVER_PROPERTY_TYPE
 - DNS_SERVER_PROPERTY_TYPE
---

## -description

Defines constants that specify the validity of the property held in the [DNS_SERVER_PROPERTY::Property](ns-netioapi-dns_server_property.md) member.

## -enum-fields

### -field DnsServerInvalidProperty:0

Specifies that the [DNS_SERVER_PROPERTY::Property](ns-netioapi-dns_server_property.md) member doesn't contain a valid DNS server property.

### -field DnsServerDohProperty

Specifies that the *DohSettings* union member contained in the [DNS_SERVER_PROPERTY::Property](ns-netioapi-dns_server_property.md) member points to a valid DNS-over-HTTPS server property.

## -remarks

## -see-also

* [DNS_SERVER_PROPERTY](ns-netioapi-dns_server_property.md)
