---
UID: NE:d3dcommon.D3D_TESSELLATOR_PARTITIONING
title: D3D_TESSELLATOR_PARTITIONING (d3dcommon.h)
description: Partitioning options.
helpviewer_keywords: ["16a23b17-fc5e-3839-422e-8dec8dda3e55","D3D11_TESSELLATOR_PARTITIONING","D3D11_TESSELLATOR_PARTITIONING enumeration [Direct3D 11]","D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN","D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD","D3D11_TESSELLATOR_PARTITIONING_INTEGER","D3D11_TESSELLATOR_PARTITIONING_POW2","D3D11_TESSELLATOR_PARTITIONING_UNDEFINED","D3D_TESSELLATOR_PARTITIONING","d3d11shader/D3D11_TESSELLATOR_PARTITIONING","d3d11shader/D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN","d3d11shader/D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD","d3d11shader/D3D11_TESSELLATOR_PARTITIONING_INTEGER","d3d11shader/D3D11_TESSELLATOR_PARTITIONING_POW2","d3d11shader/D3D11_TESSELLATOR_PARTITIONING_UNDEFINED","d3dcommon/D3D11_TESSELLATOR_PARTITIONING","d3dcommon/D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN","d3dcommon/D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD","d3dcommon/D3D11_TESSELLATOR_PARTITIONING_INTEGER","d3dcommon/D3D11_TESSELLATOR_PARTITIONING_POW2","d3dcommon/D3D11_TESSELLATOR_PARTITIONING_UNDEFINED","direct3d11.d3d11_tessellator_partitioning"]
old-location: direct3d11\d3d11_tessellator_partitioning.htm
tech.root: direct3d11
ms.assetid: 434155e2-fb96-4de7-9840-bfa8b4f2a6ce
ms.date: 12/05/2018
ms.keywords: 16a23b17-fc5e-3839-422e-8dec8dda3e55, D3D11_TESSELLATOR_PARTITIONING, D3D11_TESSELLATOR_PARTITIONING enumeration [Direct3D 11], D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN, D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD, D3D11_TESSELLATOR_PARTITIONING_INTEGER, D3D11_TESSELLATOR_PARTITIONING_POW2, D3D11_TESSELLATOR_PARTITIONING_UNDEFINED, D3D_TESSELLATOR_PARTITIONING, d3d11shader/D3D11_TESSELLATOR_PARTITIONING, d3d11shader/D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN, d3d11shader/D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD, d3d11shader/D3D11_TESSELLATOR_PARTITIONING_INTEGER, d3d11shader/D3D11_TESSELLATOR_PARTITIONING_POW2, d3d11shader/D3D11_TESSELLATOR_PARTITIONING_UNDEFINED, d3dcommon/D3D11_TESSELLATOR_PARTITIONING, d3dcommon/D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN, d3dcommon/D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD, d3dcommon/D3D11_TESSELLATOR_PARTITIONING_INTEGER, d3dcommon/D3D11_TESSELLATOR_PARTITIONING_POW2, d3dcommon/D3D11_TESSELLATOR_PARTITIONING_UNDEFINED, direct3d11.d3d11_tessellator_partitioning
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
req.typenames: D3D_TESSELLATOR_PARTITIONING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D_TESSELLATOR_PARTITIONING
 - d3dcommon/D3D_TESSELLATOR_PARTITIONING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11Shader.h
 - d3dcommon.h
api_name:
 - D3D11_TESSELLATOR_PARTITIONING
---

# D3D_TESSELLATOR_PARTITIONING enumeration


## -description

Partitioning options.

## -enum-fields

### -field D3D_TESSELLATOR_PARTITIONING_UNDEFINED:0

### -field D3D_TESSELLATOR_PARTITIONING_INTEGER:1

### -field D3D_TESSELLATOR_PARTITIONING_POW2:2

### -field D3D_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD:3

### -field D3D_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN:4

### -field D3D11_TESSELLATOR_PARTITIONING_UNDEFINED

The partitioning type is undefined.

### -field D3D11_TESSELLATOR_PARTITIONING_INTEGER

Partition with integers only.

### -field D3D11_TESSELLATOR_PARTITIONING_POW2

Partition with a power-of-two number only.

### -field D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_ODD

Partition with an odd, fractional number.

### -field D3D11_TESSELLATOR_PARTITIONING_FRACTIONAL_EVEN

Partition with an even, fractional number.

## -remarks

During tessellation, the partition option helps to determine how the algorithm chooses the next partition value; this enumeration is used by <a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_desc">D3D11_SHADER_DESC</a>.

The      <b>D3D11_TESSELLATOR_PARTITIONING</b> enumeration is type defined in the  D3D11Shader.h header file as a <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_partitioning">D3D_TESSELLATOR_PARTITIONING</a> enumeration, which is fully defined in the  D3DCommon.h header file.


```

typedef D3D_TESSELLATOR_PARTITIONING D3D11_TESSELLATOR_PARTITIONING;
```

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-enums">Shader Enumerations</a>
