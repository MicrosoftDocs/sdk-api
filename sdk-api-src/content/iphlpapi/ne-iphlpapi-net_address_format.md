---
UID: NE:iphlpapi.NET_ADDRESS_FORMAT_
title: NET_ADDRESS_FORMAT (iphlpapi.h)
description: The NET_ADDRESS_FORMAT enumeration specifies the format of a network address returned by the ParseNetworkString function.
helpviewer_keywords: ["NET_ADDRESS_DNS_NAME","NET_ADDRESS_FORMAT","NET_ADDRESS_FORMAT enumeration [IP Helper]","NET_ADDRESS_FORMAT_UNSPECIFIED","NET_ADDRESS_IPV4","NET_ADDRESS_IPV6","iphlp.net_address_format","iphlpapi/NET_ADDRESS_DNS_NAME","iphlpapi/NET_ADDRESS_FORMAT","iphlpapi/NET_ADDRESS_FORMAT_UNSPECIFIED","iphlpapi/NET_ADDRESS_IPV4","iphlpapi/NET_ADDRESS_IPV6"]
old-location: iphlp\net_address_format.htm
tech.root: IpHlp
ms.assetid: a99df758-d46e-452d-acf8-d2cb5a6fa22e
ms.date: 12/05/2018
ms.keywords: NET_ADDRESS_DNS_NAME, NET_ADDRESS_FORMAT, NET_ADDRESS_FORMAT enumeration [IP Helper], NET_ADDRESS_FORMAT_UNSPECIFIED, NET_ADDRESS_IPV4, NET_ADDRESS_IPV6, iphlp.net_address_format, iphlpapi/NET_ADDRESS_DNS_NAME, iphlpapi/NET_ADDRESS_FORMAT, iphlpapi/NET_ADDRESS_FORMAT_UNSPECIFIED, iphlpapi/NET_ADDRESS_IPV4, iphlpapi/NET_ADDRESS_IPV6
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: NET_ADDRESS_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NET_ADDRESS_FORMAT_
 - iphlpapi/NET_ADDRESS_FORMAT_
 - NET_ADDRESS_FORMAT
 - iphlpapi/NET_ADDRESS_FORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iphlpapi.h
api_name:
 - NET_ADDRESS_FORMAT
---

# NET_ADDRESS_FORMAT enumeration


## -description

The <b>NET_ADDRESS_FORMAT</b> enumeration specifies the format of a network address returned by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-parsenetworkstring">ParseNetworkString</a> function.

## -enum-fields

### -field NET_ADDRESS_FORMAT_UNSPECIFIED:0

The format of the network address is unspecified.

### -field NET_ADDRESS_DNS_NAME

The format of the network address is a DNS name.

### -field NET_ADDRESS_IPV4

The format of the network address is a string in Internet standard dotted-decimal notation for IPv4.

### -field NET_ADDRESS_IPV6

The format of the network address is a string in Internet standard hexadecimal encoding for IPv6.

## -remarks

The <b>NET_ADDRESS_FORMAT</b> enumeration is defined on Windows Vista and later. 

The [NET_ADDRESS_INFO](/windows/desktop/api/iphlpapi/ns-iphlpapi-net_address_info) structure returned by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-parsenetworkstring">ParseNetworkString</a> function.

## -see-also

[NET_ADDRESS_INFO](/windows/desktop/api/iphlpapi/ns-iphlpapi-net_address_info)



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-parsenetworkstring">ParseNetworkString</a>
