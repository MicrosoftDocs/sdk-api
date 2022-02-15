---
UID: NE:d3d12.D3D12_HEAP_SERIALIZATION_TIER
title: D3D12_HEAP_SERIALIZATION_TIER
description: Defines constants that specify heap serialization support.
tech.root: direct3d12
helpviewer_keywords: ["D3D12_HEAP_SERIALIZATION_TIER"]
ms.date: 05/20/2019
ms.keywords: D3D12_HEAP_SERIALIZATION_TIER
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
f1_keywords:
 - D3D12_HEAP_SERIALIZATION_TIER
 - d3d12/D3D12_HEAP_SERIALIZATION_TIER
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_HEAP_SERIALIZATION_TIER
---

## -description

Defines constants that specify heap serialization support.

## -enum-fields

### -field D3D12_HEAP_SERIALIZATION_TIER_0 (0)

Indicates that heap serialization is not supported.

### -field D3D12_HEAP_SERIALIZATION_TIER_10 (10)

Indicates that heap serialization is supported. Your application can serialize resource data in heaps through copying APIs such as [CopyResource](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource), without necessarily requiring an explicit [state transition](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12#implicit-state-transitions) of resources on those heaps.

## -remarks

## -see-also

