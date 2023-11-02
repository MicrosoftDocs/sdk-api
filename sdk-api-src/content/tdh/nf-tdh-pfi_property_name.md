---
UID: NF:tdh.PFI_PROPERTY_NAME
tech.root: ETW
title: PFI_PROPERTY_NAME (tdh.h)
ms.date: 12/05/2022
ms.keywords: PFI_PROPERTY_NAME
targetos: Windows
description: Macro that retrieves the Provider Field Information (PFI) property name.
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
 - PFI_PROPERTY_NAME
f1_keywords:
 - PFI_PROPERTY_NAME
 - tdh/PFI_PROPERTY_NAME
dev_langs:
 - c++
helpviewer_keywords:
 - PFI_PROPERTY_NAME
---

# PFI_PROPERTY_NAME function (tdh.h)

## -description

Macro that retrieves the Provider Field Information (PFI) property name.

## -parameters

### -param FilterInfo [in]

Provider filter info ([PROVIDER_FILTER_INFO structure](ns-tdh-provider_filter_info.md)).

### -param Property [in]

Provider property info ([EVENT_PROPERTY_INFO structure](ns-tdh-event_property_info.md)).

## -returns

The Provider Field Information (PFI) property name, or NULL.

## -remarks

## -see-also
