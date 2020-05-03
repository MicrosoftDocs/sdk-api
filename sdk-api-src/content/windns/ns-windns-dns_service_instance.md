---
UID: NS:windns._DNS_SERVICE_INSTANCE
title: DNS_SERVICE_INSTANCE structure
description: Represents a DNS service running on the network.helpviewer_keywords: ["_DNS_SERVICE_INSTANCE","DNS_SERVICE_INSTANCE"]
ms.date: 02/19/2019
ms.keywords: _DNS_SERVICE_INSTANCE, DNS_SERVICE_INSTANCE
f1_keywords:
- windns/_DNS_SERVICE_INSTANCE
dev_langs:
- c++
targetos: Windows
req.assembly: 
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: windns.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.typenames: DNS_SERVICE_INSTANCE, *PDNS_SERVICE_INSTANCE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
- apiref
api_type:
- HeaderDef
api_location:
- windns.h
api_name:
- _DNS_SERVICE_INSTANCE
- DNS_SERVICE_INSTANCE
ms.custom: 19H1
---

## -description
Represents a DNS service running on the network.

## -struct-fields

### -field pszInstanceName
A string that represents the service name. This is a fully qualified domain name that begins with a service name, and ends with ".local". It takes the generalized form "\<ServiceName\>.\_\<ServiceType\>.\_\<TransportProtocol\>.local". For example, "MyMusicServer._http._tcp.local".

### -field pszHostName
A string that represents the name of the host of the service.

### -field ip4Address
A pointer to an **IP4_ADDRESS** structure that represents the service-associated IPv4 address.

### -field ip6Address
A pointer to an [IP6_ADDRESS](/windows/desktop/api/windns/ns-windns-ip6_address_1) structure that represents the service-associated IPv6 address.

### -field wPort
A value that represents the port on which the service is running.

### -field wPriority
A value that represents the service priority.

### -field wWeight
A value that represents the service weight.

### -field dwPropertyCount
The number of properties&mdash;defines the number of elements in the arrays of the `keys` and `values` parameters.

### -param keys
A pointer to an array of string values that represent the property keys.

### -param values
A pointer to an array of string values that represent the corresponding property values.

### -field dwInterfaceIndex
A value that contains the interface index on which the service was discovered.

## -remarks
`pszInstanceName`. A string that represents the service name. This is a fully qualified domain name that begins with a service name, and ends with ".local". It takes the generalized form "\<ServiceName\>.\_\<ServiceType\>.\_\<TransportProtocol\>.local". For example, "MyMusicServer._http._tcp.local".

`pszHostName`. A string that represents the name of the host of the service.

`keys`. A pointer to an array of string values that represent the property keys.

 
`values`. A pointer to an array of string values that represent the corresponding property values.

## -see-also
