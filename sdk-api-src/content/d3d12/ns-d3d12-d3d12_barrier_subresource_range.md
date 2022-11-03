---
UID: NS:d3d12.D3D12_BARRIER_SUBRESOURCE_RANGE
title: D3D12_BARRIER_SUBRESOURCE_RANGE
description: Allows you to transition logically-adjacent ranges of subresources.
tech.root: direct3d12
ms.date: 11/01/2022
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D12_BARRIER_SUBRESOURCE_RANGE
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_BARRIER_SUBRESOURCE_RANGE
 - d3d12/D3D12_BARRIER_SUBRESOURCE_RANGE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_BARRIER_SUBRESOURCE_RANGE
prerelease: false
---

## -description

Allows you to transition logically-adjacent ranges of subresources.

## -struct-fields

### -field IndexOrFirstMipLevel

The index of the first mip level in the range; or a subresource index, if *NumMipLevels* is zero. If a subresource index, then you can use the value `0xffffffff` to specify all subresources.

### -field NumMipLevels

Number of mip levels in the range, or zero to indicate that *IndexOrFirstMipLevel* is a subresource index.

### -field FirstArraySlice

Index of first array slice in the range. Ignored if *NumMipLevels* is zero.

### -field NumArraySlices

Number of array slices in the range. Ignored if *NumMipLevels* is zero.

### -field FirstPlane

First plane slice in the range. Ignored if *NumMipLevels* is zero.

### -field NumPlanes

Number of plane slices in the range. Ignored if *NumMipLevels* is zero.

## -remarks

## -see-also
