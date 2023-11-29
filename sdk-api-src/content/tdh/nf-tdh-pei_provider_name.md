---
UID: NF:tdh.PEI_PROVIDER_NAME
tech.root: ETW
title: PEI_PROVIDER_NAME (tdh.h)
ms.date: 12/05/2022
ms.keywords: PEI_PROVIDER_NAME
targetos: Windows
description: Macro that retrieves the Provider Event Info (PEI) name.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: tdh.h
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
 - tdh.h
api_name:
 - PEI_PROVIDER_NAME
f1_keywords:
 - PEI_PROVIDER_NAME
 - tdh/PEI_PROVIDER_NAME
dev_langs:
 - c++
helpviewer_keywords:
 - PEI_PROVIDER_NAME
---

# PEI_PROVIDER_NAME function (tdh.h)

## -description

Macro that retrieves the Provider Event Info (PEI) name.

## -parameters

### -param ProviderEnum

The array of providers that have registered a MOF or manifest on the computer ([PROVIDER_ENUMERATION_INFO structure](ns-tdh-provider_enumeration_info.md))

### -param ProviderInfo

Provider event info ([PROVIDER_EVENT_INFO structure](ns-tdh-provider_event_info.md)).

## -returns

The provider name, or NULL.

## -remarks

## -see-also
