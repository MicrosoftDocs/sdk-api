---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS8
title: D3D12_FEATURE_DATA_D3D12_OPTIONS8
description: Indicates whether or not unaligned block-compressed textures are supported.
tech.root: direct3d12
ms.date: 07/21/2021
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS8
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS8
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS8
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS8
---

## -description

Indicates whether or not unaligned block-compressed textures are supported.

## -struct-fields

### -field UnalignedBlockTexturesSupported

Type: \_Out\_ **[BOOL](/windows/desktop/winprog/windows-data-types)**

Indicates whether or not unaligned block-compressed textures are supported.

If `false`, then Direct3D 12 requires that the dimensions of the top-level mip of a block-compressed texture are aligned to multiples of 4 (such alignment requirements do not apply to less-detailed mips). If `true`, then no such alignment requirement applies to any mip level of a block-compressed texture.

## -remarks

## -see-also
