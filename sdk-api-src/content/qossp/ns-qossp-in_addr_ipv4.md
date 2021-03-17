---
UID: NS:qossp._IN_ADDR_IPV4
title: IN_ADDR_IPV4 (qossp.h)
description: The IN_ADDR_IPV4 union stores an IPv4 address for use with RSVP FILTERSPECs.
helpviewer_keywords: ["*LPIN_ADDR_IPV4","*LPIN_ADDR_IPV4 union [QOS]","IN_ADDR_IPV4","IN_ADDR_IPV4 union [QOS]","qos.in_addr_ipv4","qossp/*LPIN_ADDR_IPV4","qossp/IN_ADDR_IPV4"]
old-location: qos\in_addr_ipv4.htm
tech.root: QOS
ms.assetid: 7e10cc9c-7ed4-449d-aeb9-21e3d75d0224
ms.date: 12/05/2018
ms.keywords: '*LPIN_ADDR_IPV4, *LPIN_ADDR_IPV4 union [QOS], IN_ADDR_IPV4, IN_ADDR_IPV4 union [QOS], qos.in_addr_ipv4, qossp/*LPIN_ADDR_IPV4, qossp/IN_ADDR_IPV4'
req.header: qossp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: IN_ADDR_IPV4, *LPIN_ADDR_IPV4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IN_ADDR_IPV4
 - qossp/_IN_ADDR_IPV4
 - LPIN_ADDR_IPV4
 - qossp/LPIN_ADDR_IPV4
 - IN_ADDR_IPV4
 - qossp/IN_ADDR_IPV4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qossp.h
api_name:
 - IN_ADDR_IPV4
---

# IN_ADDR_IPV4 structure


## -description

The <b>IN_ADDR_IPV4</b> union stores an IPv4 address for use with RSVP FILTERSPECs.

## -struct-fields

### -field Addr

IPv4 address, expressed as a ULONG.

### -field AddrBytes

IPv4 address, expressed as four UCHARs.

## -remarks

When working with IPv6 addresses, use <a href="/windows/desktop/api/qossp/ns-qossp-in_addr_ipv6">IN_ADDR_IPV6</a>.

## -see-also

<a href="/windows/desktop/api/qossp/ns-qossp-in_addr_ipv6">IN_ADDR_IPV6</a>