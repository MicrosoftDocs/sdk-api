---
UID: NE:d3d11_3.D3D11_TEXTURE_LAYOUT
title: D3D11_TEXTURE_LAYOUT (d3d11_3.h)
description: Specifies texture layout options.
helpviewer_keywords: ["D3D11_TEXTURE_LAYOUT","D3D11_TEXTURE_LAYOUT enumeration [Direct3D 11]","D3D11_TEXTURE_LAYOUT_64K_STANDARD_SWIZZLE","D3D11_TEXTURE_LAYOUT_ROW_MAJOR","D3D11_TEXTURE_LAYOUT_UNDEFINED","d3d11_3/D3D11_TEXTURE_LAYOUT","d3d11_3/D3D11_TEXTURE_LAYOUT_64K_STANDARD_SWIZZLE","d3d11_3/D3D11_TEXTURE_LAYOUT_ROW_MAJOR","d3d11_3/D3D11_TEXTURE_LAYOUT_UNDEFINED","direct3d11.d3d11_texture_layout"]
old-location: direct3d11\d3d11_texture_layout.htm
tech.root: direct3d11
ms.assetid: E7786550-99FC-4F8E-B93F-C2877C052EC2
ms.date: 12/05/2018
ms.keywords: D3D11_TEXTURE_LAYOUT, D3D11_TEXTURE_LAYOUT enumeration [Direct3D 11], D3D11_TEXTURE_LAYOUT_64K_STANDARD_SWIZZLE, D3D11_TEXTURE_LAYOUT_ROW_MAJOR, D3D11_TEXTURE_LAYOUT_UNDEFINED, d3d11_3/D3D11_TEXTURE_LAYOUT, d3d11_3/D3D11_TEXTURE_LAYOUT_64K_STANDARD_SWIZZLE, d3d11_3/D3D11_TEXTURE_LAYOUT_ROW_MAJOR, d3d11_3/D3D11_TEXTURE_LAYOUT_UNDEFINED, direct3d11.d3d11_texture_layout
req.header: d3d11_3.h
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
req.typenames: D3D11_TEXTURE_LAYOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEXTURE_LAYOUT
 - d3d11_3/D3D11_TEXTURE_LAYOUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_3.h
api_name:
 - D3D11_TEXTURE_LAYOUT
---

# D3D11_TEXTURE_LAYOUT enumeration


## -description

Specifies texture layout options.

## -enum-fields

### -field D3D11_TEXTURE_LAYOUT_UNDEFINED:0

The texture layout is undefined, and is selected by the driver.

### -field D3D11_TEXTURE_LAYOUT_ROW_MAJOR:1

Data for the texture is stored in row major (sometimes called pitch-linear) order.

### -field D3D11_TEXTURE_LAYOUT_64K_STANDARD_SWIZZLE:2

A default texture uses the standardized swizzle pattern.

## -remarks

This enumeration controls the swizzle pattern of default textures and enable map support on default textures.  Callers must query <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options2">D3D11_FEATURE_DATA_D3D11_OPTIONS2</a> to ensure that each option is supported.

The standard swizzle formats applies within each page-sized chunk, and pages are laid out in linear order with respect to one another.  A 16-bit interleave pattern defines the conversion from pre-swizzled intra-page location to the post-swizzled location.  

<img alt="Standard swizzle patterns" src="./images/d3d11_standardswizzle.png"/>
To demonstrate, consider the 32bpp swizzle format above.  This is represented by the following interleave masks, where bits on the left are most-significant.


``` syntax
UINT xBytesMask = 1010 1010 1000 1111
UINT yMask =      0101 0101 0111 0000

```

To compute the swizzled address, the following code could be used (where the _pdep_u32 instruction is supported):


``` syntax
UINT swizzledOffset = resourceBaseOffset +
                      _pdep_u32(xOffset, xBytesMask) + 
                      _pdep_u32(yOffset, yBytesMask);

```


## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
