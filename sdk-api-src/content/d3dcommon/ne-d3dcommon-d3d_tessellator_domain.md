---
UID: NE:d3dcommon.D3D_TESSELLATOR_DOMAIN
title: D3D_TESSELLATOR_DOMAIN (d3dcommon.h)
description: Domain options for tessellator data.
helpviewer_keywords: ["D3D11_TESSELLATOR_DOMAIN","D3D11_TESSELLATOR_DOMAIN enumeration [Direct3D 11]","D3D11_TESSELLATOR_DOMAIN_ISOLINE","D3D11_TESSELLATOR_DOMAIN_QUAD","D3D11_TESSELLATOR_DOMAIN_TRI","D3D11_TESSELLATOR_DOMAIN_UNDEFINED","D3D_TESSELLATOR_DOMAIN","b9d735b7-3708-663e-40ab-0d0f519b8b89","d3d11shader/D3D11_TESSELLATOR_DOMAIN","d3d11shader/D3D11_TESSELLATOR_DOMAIN_ISOLINE","d3d11shader/D3D11_TESSELLATOR_DOMAIN_QUAD","d3d11shader/D3D11_TESSELLATOR_DOMAIN_TRI","d3d11shader/D3D11_TESSELLATOR_DOMAIN_UNDEFINED","d3dcommon/D3D11_TESSELLATOR_DOMAIN","d3dcommon/D3D11_TESSELLATOR_DOMAIN_ISOLINE","d3dcommon/D3D11_TESSELLATOR_DOMAIN_QUAD","d3dcommon/D3D11_TESSELLATOR_DOMAIN_TRI","d3dcommon/D3D11_TESSELLATOR_DOMAIN_UNDEFINED","direct3d11.d3d11_tessellator_domain"]
old-location: direct3d11\d3d11_tessellator_domain.htm
tech.root: direct3d11
ms.assetid: d0c9ea8a-a1e2-44c3-a4ac-bdc43e5171b5
ms.date: 12/05/2018
ms.keywords: D3D11_TESSELLATOR_DOMAIN, D3D11_TESSELLATOR_DOMAIN enumeration [Direct3D 11], D3D11_TESSELLATOR_DOMAIN_ISOLINE, D3D11_TESSELLATOR_DOMAIN_QUAD, D3D11_TESSELLATOR_DOMAIN_TRI, D3D11_TESSELLATOR_DOMAIN_UNDEFINED, D3D_TESSELLATOR_DOMAIN, b9d735b7-3708-663e-40ab-0d0f519b8b89, d3d11shader/D3D11_TESSELLATOR_DOMAIN, d3d11shader/D3D11_TESSELLATOR_DOMAIN_ISOLINE, d3d11shader/D3D11_TESSELLATOR_DOMAIN_QUAD, d3d11shader/D3D11_TESSELLATOR_DOMAIN_TRI, d3d11shader/D3D11_TESSELLATOR_DOMAIN_UNDEFINED, d3dcommon/D3D11_TESSELLATOR_DOMAIN, d3dcommon/D3D11_TESSELLATOR_DOMAIN_ISOLINE, d3dcommon/D3D11_TESSELLATOR_DOMAIN_QUAD, d3dcommon/D3D11_TESSELLATOR_DOMAIN_TRI, d3dcommon/D3D11_TESSELLATOR_DOMAIN_UNDEFINED, direct3d11.d3d11_tessellator_domain
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
req.typenames: D3D_TESSELLATOR_DOMAIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D_TESSELLATOR_DOMAIN
 - d3dcommon/D3D_TESSELLATOR_DOMAIN
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
 - D3D11_TESSELLATOR_DOMAIN
---

# D3D_TESSELLATOR_DOMAIN enumeration


## -description

Domain options for tessellator data.

## -enum-fields

### -field D3D_TESSELLATOR_DOMAIN_UNDEFINED:0

### -field D3D_TESSELLATOR_DOMAIN_ISOLINE:1

### -field D3D_TESSELLATOR_DOMAIN_TRI:2

### -field D3D_TESSELLATOR_DOMAIN_QUAD:3

### -field D3D11_TESSELLATOR_DOMAIN_UNDEFINED

The data type is undefined.

### -field D3D11_TESSELLATOR_DOMAIN_ISOLINE

Isoline data.

### -field D3D11_TESSELLATOR_DOMAIN_TRI

Triangle data.

### -field D3D11_TESSELLATOR_DOMAIN_QUAD

Quad data.

## -remarks

The data domain defines the type of data. This enumeration is used by <a href="/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_desc">D3D11_SHADER_DESC</a>.

The <b>D3D11_TESSELLATOR_DOMAIN</b>     enumeration is type defined in the  D3D11Shader.h header file as a <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_tessellator_domain">D3D_TESSELLATOR_DOMAIN</a> enumeration, which is fully defined in the  D3DCommon.h header file.


```

typedef D3D_TESSELLATOR_DOMAIN D3D11_TESSELLATOR_DOMAIN;
```

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-enums">Shader Enumerations</a>
