---
UID: NS:netioapi._DNS_SERVER_PROPERTY_TYPES
title: DNS_SERVER_PROPERTY_TYPES
description: Contains a pointer to a DNS server property. The type of the property depends on the value of [DNS_SERVER_PROPERTY::Type](/windows/win32/api/netioapi/ns-netioapi-dns_server_property).
tech.root: IpHlp
ms.date: 07/16/2021
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
req.typenames: DNS_SERVER_PROPERTY_TYPES
req.redist: 
f1_keywords:
 - _DNS_SERVER_PROPERTY_TYPES
 - netioapi/_DNS_SERVER_PROPERTY_TYPES
 - DNS_SERVER_PROPERTY_TYPES
 - netioapi/DNS_SERVER_PROPERTY_TYPES
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netioapi.h
api_name:
 - _DNS_SERVER_PROPERTY_TYPES
 - DNS_SERVER_PROPERTY_TYPES
---

## -description

Contains a pointer to a DNS server property. The type of the property depends on the value of [DNS_SERVER_PROPERTY::Type](/windows/win32/api/netioapi/ns-netioapi-dns_server_property).

## -struct-fields

### -field DohSettings

If [DNS_SERVER_PROPERTY::Type](ns-netioapi-dns_server_property.md) is set to *DnsServerDohProperty*, then *DohSettings* points to a valid DNS-over-HTTPS server property.

## -remarks

## -see-also

* [DNS_SERVER_PROPERTY](ns-netioapi-dns_server_property.md)
