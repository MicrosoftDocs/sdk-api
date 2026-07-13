---
UID: NE:d3dcommon.D3D_TESSELLATOR_OUTPUT_PRIMITIVE
title: D3D_TESSELLATOR_OUTPUT_PRIMITIVE (d3dcommon.h)
description: Output primitive types.
helpviewer_keywords: ["8cfde449-9de7-6aec-645e-eaa2eafd531f","D3D11_TESSELLATOR_OUTPUT_LINE","D3D11_TESSELLATOR_OUTPUT_POINT","D3D11_TESSELLATOR_OUTPUT_PRIMITIVE","D3D11_TESSELLATOR_OUTPUT_PRIMITIVE enumeration [Direct3D 11]","D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CCW","D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CW","D3D11_TESSELLATOR_OUTPUT_UNDEFINED","D3D_TESSELLATOR_OUTPUT_PRIMITIVE","d3d11shader/D3D11_TESSELLATOR_OUTPUT_LINE","d3d11shader/D3D11_TESSELLATOR_OUTPUT_POINT","d3d11shader/D3D11_TESSELLATOR_OUTPUT_PRIMITIVE","d3d11shader/D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CCW","d3d11shader/D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CW","d3d11shader/D3D11_TESSELLATOR_OUTPUT_UNDEFINED","d3dcommon/D3D11_TESSELLATOR_OUTPUT_LINE","d3dcommon/D3D11_TESSELLATOR_OUTPUT_POINT","d3dcommon/D3D11_TESSELLATOR_OUTPUT_PRIMITIVE","d3dcommon/D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CCW","d3dcommon/D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CW","d3dcommon/D3D11_TESSELLATOR_OUTPUT_UNDEFINED","direct3d11.d3d11_tessellator_output_primitive"]
old-location: direct3d11\d3d11_tessellator_output_primitive.htm
tech.root: direct3d11
ms.assetid: 6dc6d48d-bb93-4961-9fb4-6e3be194fae8
ms.date: 12/05/2018
ms.keywords: 8cfde449-9de7-6aec-645e-eaa2eafd531f, D3D11_TESSELLATOR_OUTPUT_LINE, D3D11_TESSELLATOR_OUTPUT_POINT, D3D11_TESSELLATOR_OUTPUT_PRIMITIVE, D3D11_TESSELLATOR_OUTPUT_PRIMITIVE enumeration [Direct3D 11], D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CCW, D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CW, D3D11_TESSELLATOR_OUTPUT_UNDEFINED, D3D_TESSELLATOR_OUTPUT_PRIMITIVE, d3d11shader/D3D11_TESSELLATOR_OUTPUT_LINE, d3d11shader/D3D11_TESSELLATOR_OUTPUT_POINT, d3d11shader/D3D11_TESSELLATOR_OUTPUT_PRIMITIVE, d3d11shader/D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CCW, d3d11shader/D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CW, d3d11shader/D3D11_TESSELLATOR_OUTPUT_UNDEFINED, d3dcommon/D3D11_TESSELLATOR_OUTPUT_LINE, d3dcommon/D3D11_TESSELLATOR_OUTPUT_POINT, d3dcommon/D3D11_TESSELLATOR_OUTPUT_PRIMITIVE, d3dcommon/D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CCW, d3dcommon/D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CW, d3dcommon/D3D11_TESSELLATOR_OUTPUT_UNDEFINED, direct3d11.d3d11_tessellator_output_primitive
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
req.typenames: D3D_TESSELLATOR_OUTPUT_PRIMITIVE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D_TESSELLATOR_OUTPUT_PRIMITIVE
 - d3dcommon/D3D_TESSELLATOR_OUTPUT_PRIMITIVE
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
 - D3D11_TESSELLATOR_OUTPUT_PRIMITIVE
---

# D3D_TESSELLATOR_OUTPUT_PRIMITIVE enumeration


## -description

Output primitive types.

## -enum-fields

### -field D3D_TESSELLATOR_OUTPUT_UNDEFINED:0

### -field D3D_TESSELLATOR_OUTPUT_POINT:1

### -field D3D_TESSELLATOR_OUTPUT_LINE:2

### -field D3D_TESSELLATOR_OUTPUT_TRIANGLE_CW:3

### -field D3D_TESSELLATOR_OUTPUT_TRIANGLE_CCW:4

### -field D3D11_TESSELLATOR_OUTPUT_UNDEFINED

The output primitive type is undefined.

### -field D3D11_TESSELLATOR_OUTPUT_POINT

The output primitive type is a point.

### -field D3D11_TESSELLATOR_OUTPUT_LINE

The output primitive type is a line.

### -field D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CW

The output primitive type is a clockwise triangle.

### -field D3D11_TESSELLATOR_OUTPUT_TRIANGLE_CCW

The output primitive type is a counter clockwise triangle.

## -remarks

The output primitive type determines how the tessellator output data is organized; this enumeration is used by <a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_desc">D3D11_SHADER_DESC</a>.

The <b>D3D11_TESSELLATOR_OUTPUT_PRIMITIVE</b>     enumeration is type defined in the  D3D11Shader.h header file as a <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_output_primitive">D3D_TESSELLATOR_OUTPUT_PRIMITIVE</a> enumeration, which is fully defined in the  D3DCommon.h header file.


```

typedef D3D_TESSELLATOR_OUTPUT_PRIMITIVE D3D11_TESSELLATOR_OUTPUT_PRIMITIVE;
```

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-enums">Shader Enumerations</a>
