---
UID: NF:tdh.EMI_MAP_OUTPUT
tech.root: ETW
title: EMI_MAP_OUTPUT (tdh.h)
ms.date: 12/05/2022
ms.keywords: EMI_MAP_OUTPUT
targetos: Windows
description: Macro that retrieves the event map output.
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
 - EMI_MAP_OUTPUT
f1_keywords:
 - EMI_MAP_OUTPUT
 - tdh/EMI_MAP_OUTPUT
dev_langs:
 - c++
helpviewer_keywords:
 - EMI_MAP_OUTPUT
---

# EMI_MAP_OUTPUT function (tdh.h)

## -description

Macro that retrieves the event map output.

## -parameters

### -param MapInfo

The metadata about the event map ([EVENT_MAP_INFO structure](ns-tdh-event_map_info.md)).

### -param Map

A single value map entry ([EVENT_MAP_ENTRY structure](ns-tdh-event_map_entry.md)).

## -returns

The event map output, or NULL.

## -remarks

## -see-also
