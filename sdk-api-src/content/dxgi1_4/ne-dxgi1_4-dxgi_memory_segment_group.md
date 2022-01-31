---
UID: NE:dxgi1_4.DXGI_MEMORY_SEGMENT_GROUP
title: DXGI_MEMORY_SEGMENT_GROUP (dxgi1_4.h)
description: Specifies the memory segment group to use.
helpviewer_keywords: ["DXGI_MEMORY_SEGMENT_GROUP","DXGI_MEMORY_SEGMENT_GROUP enumeration [DXGI]","DXGI_MEMORY_SEGMENT_GROUP_LOCAL","DXGI_MEMORY_SEGMENT_GROUP_NON_LOCAL","direct3ddxgi.dxgi_memory_segment_group","dxgi1_4/DXGI_MEMORY_SEGMENT_GROUP","dxgi1_4/DXGI_MEMORY_SEGMENT_GROUP_LOCAL","dxgi1_4/DXGI_MEMORY_SEGMENT_GROUP_NON_LOCAL"]
old-location: direct3ddxgi\dxgi_memory_segment_group.htm
tech.root: direct3ddxgi
ms.assetid: 2FE35513-040E-41BF-866E-A13679C4F322
ms.date: 12/05/2018
ms.keywords: DXGI_MEMORY_SEGMENT_GROUP, DXGI_MEMORY_SEGMENT_GROUP enumeration [DXGI], DXGI_MEMORY_SEGMENT_GROUP_LOCAL, DXGI_MEMORY_SEGMENT_GROUP_NON_LOCAL, direct3ddxgi.dxgi_memory_segment_group, dxgi1_4/DXGI_MEMORY_SEGMENT_GROUP, dxgi1_4/DXGI_MEMORY_SEGMENT_GROUP_LOCAL, dxgi1_4/DXGI_MEMORY_SEGMENT_GROUP_NON_LOCAL
req.header: dxgi1_4.h
req.include-header: DXGI1_3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DXGI_MEMORY_SEGMENT_GROUP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_MEMORY_SEGMENT_GROUP
 - dxgi1_4/DXGI_MEMORY_SEGMENT_GROUP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_4.h
api_name:
 - DXGI_MEMORY_SEGMENT_GROUP
---

# DXGI_MEMORY_SEGMENT_GROUP enumeration


## -description

Specifies the memory segment group to use.

## -enum-fields

### -field DXGI_MEMORY_SEGMENT_GROUP_LOCAL:0

              The grouping of segments which is considered local to the video adapter, and represents the fastest available memory to the GPU. Applications should target the local segment group as the target size for their working set.

### -field DXGI_MEMORY_SEGMENT_GROUP_NON_LOCAL:1

The grouping of segments which is considered non-local to the video adapter, and may have slower performance than the local segment group.

## -remarks

This enum is used by <a href="/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo">QueryVideoMemoryInfo</a> and <a href="/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-setvideomemoryreservation">SetVideoMemoryReservation</a>.

Refer to the remarks for <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool">D3D12_MEMORY_POOL</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>
