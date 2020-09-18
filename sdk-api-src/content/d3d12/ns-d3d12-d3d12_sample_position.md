---
UID: NS:d3d12.D3D12_SAMPLE_POSITION
title: D3D12_SAMPLE_POSITION (d3d12.h)
description: Describes a sub-pixel sample position for use with programmable sample positions.
helpviewer_keywords: ["D3D12_SAMPLE_POSITION","D3D12_SAMPLE_POSITION structure","d3d12/D3D12_SAMPLE_POSITION","direct3d12.d3d12_sample_position"]
old-location: direct3d12\d3d12_sample_position.htm
tech.root: direct3d12
ms.assetid: 09D76360-A5FC-43C5-A7DC-9FA59B7FA94D
ms.date: 12/05/2018
ms.keywords: D3D12_SAMPLE_POSITION, D3D12_SAMPLE_POSITION structure, d3d12/D3D12_SAMPLE_POSITION, direct3d12.d3d12_sample_position
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
req.typenames: D3D12_SAMPLE_POSITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_SAMPLE_POSITION
 - d3d12/D3D12_SAMPLE_POSITION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_SAMPLE_POSITION
---

# D3D12_SAMPLE_POSITION structure


## -description

Describes a sub-pixel sample position for use with programmable sample positions.

## -struct-fields

### -field X

A signed sub-pixel coordinate value in the X axis.

### -field Y

A signed sub-pixel coordinate value in the Y axis.

## -remarks

Sample positions have the origin (0, 0) at the pixel center. Each of the X and Y coordinates are signed values in the range -8 (top/left) to 7 (bottom/right). Values outside this range are invalid.

Each increment of these integer values represents 1/16th of a pixel. For example, X and Y values of -8 and 4, respectively, correspond to floating-point values of -0.5 and 0.25, a point located on the left-most edge of the pixel, half-way between its center-line and the bottom edge. Because of this, the bottom-most and right-most edge of a pixel are not reachable by sampling (these positions are reachable as the top-most and left-most edges of the neighboring pixels).

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>