---
UID: NF:evntcons.EtwGetTraitFromProviderTraits
tech.root: ETW
title: EtwGetTraitFromProviderTraits (evntcons.h)
ms.date: 11/28/2022
ms.keywords: EtwGetTraitFromProviderTraits
targetos: Windows
description: 
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: evntcons.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - evntcons.h
api_name:
 - EtwGetTraitFromProviderTraits
f1_keywords:
 - EtwGetTraitFromProviderTraits
 - evntcons/EtwGetTraitFromProviderTraits
dev_langs:
 - c++
helpviewer_keywords:
 - EtwGetTraitFromProviderTraits
---

# EtwGetTraitFromProviderTraits function (evntcons.h)

## -description

Retrieves an individual trait from the ETW provider.

## -parameters

### -param ProviderTraits [in]

The Provider traits.

### -param TraitType [in]

The [ETW_PROVIDER_TRAIT_TYPE](ne-evntcons-etw_provider_trait_type.md).

### -param Trait [out]

The Provider trait.

### -param Size [out]

The trait size.

## -returns

Returns ERROR_SUCCESS if successful.

## -remarks

Providers are applications that can generate event logs.

## -see-also
