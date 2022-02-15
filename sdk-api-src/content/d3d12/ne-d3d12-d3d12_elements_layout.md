---
UID: NE:d3d12.D3D12_ELEMENTS_LAYOUT
title: D3D12_ELEMENTS_LAYOUT (d3d12.h)
description: Describes how the locations of elements are identified.
helpviewer_keywords: ["D3D12_ELEMENTS_LAYOUT","D3D12_ELEMENTS_LAYOUT enumeration","D3D12_ELEMENTS_LAYOUT_ARRAY","D3D12_ELEMENTS_LAYOUT_ARRAY_OF_POINTERS","d3d12/D3D12_ELEMENTS_LAYOUT","d3d12/D3D12_ELEMENTS_LAYOUT_ARRAY","d3d12/D3D12_ELEMENTS_LAYOUT_ARRAY_OF_POINTERS","direct3d12.d3d12_elements_layout"]
old-location: direct3d12\d3d12_elements_layout.htm
tech.root: direct3d12
ms.assetid: C3BEAE37-3C3B-4128-95C1-DD88B31AC5A3
ms.date: 12/05/2018
ms.keywords: D3D12_ELEMENTS_LAYOUT, D3D12_ELEMENTS_LAYOUT enumeration, D3D12_ELEMENTS_LAYOUT_ARRAY, D3D12_ELEMENTS_LAYOUT_ARRAY_OF_POINTERS, d3d12/D3D12_ELEMENTS_LAYOUT, d3d12/D3D12_ELEMENTS_LAYOUT_ARRAY, d3d12/D3D12_ELEMENTS_LAYOUT_ARRAY_OF_POINTERS, direct3d12.d3d12_elements_layout
req.header: d3d12.h
req.include-header: 
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
req.typenames: D3D12_ELEMENTS_LAYOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_ELEMENTS_LAYOUT
 - d3d12/D3D12_ELEMENTS_LAYOUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_ELEMENTS_LAYOUT
---

# D3D12_ELEMENTS_LAYOUT enumeration


## -description

Describes how the locations of elements are identified.

## -enum-fields

### -field D3D12_ELEMENTS_LAYOUT_ARRAY:0

For a data set of <i>n</i> elements, the pointer parameter points to the start of <i>n</i> elements in memory.

### -field D3D12_ELEMENTS_LAYOUT_ARRAY_OF_POINTERS:0x1

For a data set of <i>n</i> elements, the pointer parameter points to an array of <i>n</i> pointers in memory, each pointing to an individual element of the set.

