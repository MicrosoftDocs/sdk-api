---
UID: NE:d3d10.D3D10_RESOURCE_DIMENSION
title: D3D10_RESOURCE_DIMENSION (d3d10.h)
description: Identifies the type of resource being used.
helpviewer_keywords: ["63b970df-266a-f05f-9db6-cec5c9ae14a6","D3D10_RESOURCE_DIMENSION","D3D10_RESOURCE_DIMENSION enumeration [Direct3D 10]","D3D10_RESOURCE_DIMENSION_BUFFER","D3D10_RESOURCE_DIMENSION_TEXTURE1D","D3D10_RESOURCE_DIMENSION_TEXTURE2D","D3D10_RESOURCE_DIMENSION_TEXTURE3D","D3D10_RESOURCE_DIMENSION_UNKNOWN","d3d10/D3D10_RESOURCE_DIMENSION","d3d10/D3D10_RESOURCE_DIMENSION_BUFFER","d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE1D","d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE2D","d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE3D","d3d10/D3D10_RESOURCE_DIMENSION_UNKNOWN","direct3d10.d3d10_resource_dimension"]
old-location: direct3d10\d3d10_resource_dimension.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_resource_dimension.htm
ms.date: 12/05/2018
ms.keywords: 63b970df-266a-f05f-9db6-cec5c9ae14a6, D3D10_RESOURCE_DIMENSION, D3D10_RESOURCE_DIMENSION enumeration [Direct3D 10], D3D10_RESOURCE_DIMENSION_BUFFER, D3D10_RESOURCE_DIMENSION_TEXTURE1D, D3D10_RESOURCE_DIMENSION_TEXTURE2D, D3D10_RESOURCE_DIMENSION_TEXTURE3D, D3D10_RESOURCE_DIMENSION_UNKNOWN, d3d10/D3D10_RESOURCE_DIMENSION, d3d10/D3D10_RESOURCE_DIMENSION_BUFFER, d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE1D, d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE2D, d3d10/D3D10_RESOURCE_DIMENSION_TEXTURE3D, d3d10/D3D10_RESOURCE_DIMENSION_UNKNOWN, direct3d10.d3d10_resource_dimension
req.header: d3d10.h
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
req.typenames: D3D10_RESOURCE_DIMENSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_RESOURCE_DIMENSION
 - d3d10/D3D10_RESOURCE_DIMENSION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_RESOURCE_DIMENSION
---

# D3D10_RESOURCE_DIMENSION enumeration


## -description

Identifies the type of <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">resource</a> being used.

## -enum-fields

### -field D3D10_RESOURCE_DIMENSION_UNKNOWN:0

Resource is of unknown type.

### -field D3D10_RESOURCE_DIMENSION_BUFFER:1

Resource is a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffer</a>.

### -field D3D10_RESOURCE_DIMENSION_TEXTURE1D:2

Resource is a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">1D texture</a>.

### -field D3D10_RESOURCE_DIMENSION_TEXTURE2D:3

Resource is a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">2D texture</a>.

### -field D3D10_RESOURCE_DIMENSION_TEXTURE3D:4

Resource is a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">3D texture</a>.

## -remarks

This enumeration is used in <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10resource-gettype">ID3D10Resource::GetType</a>, and <a href="/windows/desktop/direct3d10/d3dx10-image-info">D3DX10_IMAGE_INFO</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-enums">Resource Enumerations</a>
