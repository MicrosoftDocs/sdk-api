---
UID: NE:d3dcommon.D3D_INTERPOLATION_MODE
title: D3D_INTERPOLATION_MODE (d3dcommon.h)
description: Specifies interpolation mode, which affects how values are calculated during rasterization.
helpviewer_keywords: ["D3D_INTERPOLATION_CONSTANT","D3D_INTERPOLATION_LINEAR","D3D_INTERPOLATION_LINEAR_CENTROID","D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE","D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_CENTROID","D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_SAMPLE","D3D_INTERPOLATION_LINEAR_SAMPLE","D3D_INTERPOLATION_MODE","D3D_INTERPOLATION_MODE enumeration [Direct3D 11]","D3D_INTERPOLATION_UNDEFINED","d3dcommon/D3D_INTERPOLATION_CONSTANT","d3dcommon/D3D_INTERPOLATION_LINEAR","d3dcommon/D3D_INTERPOLATION_LINEAR_CENTROID","d3dcommon/D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE","d3dcommon/D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_CENTROID","d3dcommon/D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_SAMPLE","d3dcommon/D3D_INTERPOLATION_LINEAR_SAMPLE","d3dcommon/D3D_INTERPOLATION_MODE","d3dcommon/D3D_INTERPOLATION_UNDEFINED","direct3d11.d3d_interpolation_mode"]
old-location: direct3d11\d3d_interpolation_mode.htm
tech.root: direct3d11
ms.assetid: E4D5F0C3-535F-4CE0-B42F-00D961C83EF1
ms.date: 12/05/2018
ms.keywords: D3D_INTERPOLATION_CONSTANT, D3D_INTERPOLATION_LINEAR, D3D_INTERPOLATION_LINEAR_CENTROID, D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE, D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_CENTROID, D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_SAMPLE, D3D_INTERPOLATION_LINEAR_SAMPLE, D3D_INTERPOLATION_MODE, D3D_INTERPOLATION_MODE enumeration [Direct3D 11], D3D_INTERPOLATION_UNDEFINED, d3dcommon/D3D_INTERPOLATION_CONSTANT, d3dcommon/D3D_INTERPOLATION_LINEAR, d3dcommon/D3D_INTERPOLATION_LINEAR_CENTROID, d3dcommon/D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE, d3dcommon/D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_CENTROID, d3dcommon/D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_SAMPLE, d3dcommon/D3D_INTERPOLATION_LINEAR_SAMPLE, d3dcommon/D3D_INTERPOLATION_MODE, d3dcommon/D3D_INTERPOLATION_UNDEFINED, direct3d11.d3d_interpolation_mode
req.header: d3dcommon.h
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
req.typenames: D3D_INTERPOLATION_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D_INTERPOLATION_MODE
 - d3dcommon/D3D_INTERPOLATION_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3DCommon.h
api_name:
 - D3D_INTERPOLATION_MODE
---

# D3D_INTERPOLATION_MODE enumeration


## -description

Specifies interpolation mode, which affects how values are calculated during rasterization.

## -enum-fields

### -field D3D_INTERPOLATION_UNDEFINED:0

The interpolation mode is undefined.

### -field D3D_INTERPOLATION_CONSTANT:1

Don't interpolate between register values.

### -field D3D_INTERPOLATION_LINEAR:2

Interpolate linearly between register values.

### -field D3D_INTERPOLATION_LINEAR_CENTROID:3

Interpolate linearly between register values but centroid clamped when multisampling.

### -field D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE:4

Interpolate linearly between register values but with no perspective correction.

### -field D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_CENTROID:5

Interpolate linearly between register values but with no perspective correction and centroid clamped when multisampling.

### -field D3D_INTERPOLATION_LINEAR_SAMPLE:6

Interpolate linearly between register values but sample clamped when multisampling.

### -field D3D_INTERPOLATION_LINEAR_NOPERSPECTIVE_SAMPLE:7

Interpolate linearly between register values but with no perspective correction and sample clamped when multisampling.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-enumerations">Common Version Enumerations</a>



<a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc">D3D11_PARAMETER_DESC</a>
