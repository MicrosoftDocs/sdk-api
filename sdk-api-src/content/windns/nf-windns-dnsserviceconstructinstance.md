---
UID: NF:windns.DnsServiceConstructInstance
title: DnsServiceConstructInstance function
description: Used to build a [DNS_SERVICE_INSTANCE](../windns/ns-windns-dns_service_instance.md) structure from data that describes it.
tech.root: dns
helpviewer_keywords: ["DnsServiceConstructInstance"]
ms.date: 02/14/2019
ms.keywords: DnsServiceConstructInstance
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: dnsapi.dll
req.header: windns.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: dnsapi.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
f1_keywords:
 - DnsServiceConstructInstance
 - windns/DnsServiceConstructInstance
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - windns.h
api_name:
 - DnsServiceConstructInstance
---

## -description

Used to build a [DNS_SERVICE_INSTANCE](/windows/win32/api/windns/ns-windns-dns_service_instance) structure from data that describes it.

## -parameters

### -param pServiceName

A string that represents the name of the service.

### -param pHostName

A string that represents the name of the host of the service.

### -param pIp4

A pointer to an **IP4_ADDRESS** structure that represents the service-associated IPv4 address.

### -param pIp6

A pointer to an [IP6_ADDRESS](/windows/win32/api/windnsdef/ns-windnsdef-ip6_address) structure that represents the service-associated IPv6 address.

### -param wPort

A value that represents the port on which the service is running.

### -param wPriority

A value that represents the service priority.

### -param wWeight

A value that represents the service weight.

### -param dwPropertiesCount

The number of properties&mdash;defines the number of elements in the arrays of the `keys` and `values` parameters.

### -param keys

A pointer to an array of string values that represent the property keys.

### -param values

A pointer to an array of string values that represent the corresponding property values.

## -returns

A pointer to a newly allocated [DNS_SERVICE_INSTANCE](ns-windns-dns_service_instance.md) structure, built from the passed-in parameters. Your application is responsible for freeing the associated memory by calling [DnsServiceFreeInstance](nf-windns-dnsservicefreeinstance.md).

## -remarks

The **dwInterfaceIndex** field of the returned structure is set to 0.

## -see-also

