---
UID: NE:evntcons.ETW_PROVIDER_TRAIT_TYPE
tech.root: ETW
title: ETW_PROVIDER_TRAIT_TYPE (evntcons.h)
ms.date: 11/28/2022
ms.keywords: ETW_PROVIDER_TRAIT_TYPE
targetos: Windows
description: Specifies the types of Provider Traits supported by Event Tracing for Windows (ETW).
req.construct-type: enumeration
req.ddi-compliance: 
req.header: evntcons.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.target-type: Windows
req.typenames: ETW_PROVIDER_TRAIT_TYPE
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - evntcons.h
api_name:
 - ETW_PROVIDER_TRAIT_TYPE
f1_keywords:
 - ETW_PROVIDER_TRAIT_TYPE
 - evntcons/ETW_PROVIDER_TRAIT_TYPE
dev_langs:
 - c++
helpviewer_keywords:
 - ETW_PROVIDER_TRAIT_TYPE
---

# ETW_PROVIDER_TRAIT_TYPE enumeration (evntcons.h)


## -description

Specifies the types of Provider Traits supported by Event Tracing for Windows (ETW).

## -enum-fields

### -field EtwProviderTraitTypeGroup

ETW Provider trait group.

### -field EtwProviderTraitDecodeGuid

ETW Provider trait decode GUID.

### -field EtwProviderTraitTypeMax

ETW Provider trait type maximum.

## -remarks

Providers are applications that can generate event logs.

## -see-also

[Provider Traits](/windows/win32/etw/provider-traits)

