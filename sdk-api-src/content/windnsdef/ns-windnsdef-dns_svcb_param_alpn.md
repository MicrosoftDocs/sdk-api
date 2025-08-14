---
UID: NS:windnsdef._DNS_SVCB_PARAM_ALPN
title: DNS_SVCB_PARAM_ALPN
description: The DNS_SVCB_PARAM_ALPN structure represents RFC 9460 section 7.1.
tech.root: DNS
ms.date: 07/03/2025
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: windnsdef.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: DNS_SVCB_PARAM_ALPN
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windnsdef.h
api_name:
 - _DNS_SVCB_PARAM_ALPN
 - DNS_SVCB_PARAM_ALPN
f1_keywords:
 - _DNS_SVCB_PARAM_ALPN
 - windnsdef/_DNS_SVCB_PARAM_ALPN
 - DNS_SVCB_PARAM_ALPN
 - windnsdef/DNS_SVCB_PARAM_ALPN
dev_langs:
 - c++
helpviewer_keywords:
 - _DNS_SVCB_PARAM_ALPN
---

## -description

The **DNS_SVCB_PARAM_ALPN** structure represents RFC 9460 section 7.1.

## -struct-fields

### -field cIds

Count of alpn ids.

### -field rgIds[1]

List of alpn id structs representing available services.

## -remarks

## -see-also
