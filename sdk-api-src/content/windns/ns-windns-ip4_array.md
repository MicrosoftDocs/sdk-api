---
UID: NS:windns._IP4_ARRAY
title: IP4_ARRAY (windns.h)
description: The IP4_ARRAY structure stores an array of IPv4 addresses.
helpviewer_keywords: ["*PIP4_ARRAY","*PIP4_ARRAY structure [DNS]","IP4_ARRAY","IP4_ARRAY structure [DNS]","dns.ip4_array","windns/*PIP4_ARRAY","windns/IP4_ARRAY"]
old-location: dns\ip4_array.htm
tech.root: DNS
ms.assetid: 4273a739-129c-4951-b6df-aef4332ce0cb
ms.date: 12/05/2018
ms.keywords: '*PIP4_ARRAY, *PIP4_ARRAY structure [DNS], IP4_ARRAY, IP4_ARRAY structure [DNS], dns.ip4_array, windns/*PIP4_ARRAY, windns/IP4_ARRAY'
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: IP4_ARRAY, *PIP4_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IP4_ARRAY
 - windns/_IP4_ARRAY
 - PIP4_ARRAY
 - windns/PIP4_ARRAY
 - IP4_ARRAY
 - windns/IP4_ARRAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - IP4_ARRAY
---

# IP4_ARRAY structure


## -description

The <b>IP4_ARRAY</b> structure stores an array of IPv4 addresses.

## -struct-fields

### -field AddrCount

The number of IPv4 addresses in <b>AddrArray</b>.

### -field AddrArray.size_is

### -field AddrArray.size_is.AddrCount

### -field AddrArray

An array of <a href="/windows/desktop/DNS/dns-data-types">IP4_ADDRESS</a> data types that contains a list of IPv4 address.