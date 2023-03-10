---
UID: NE:d2d1effectauthor.D2D1_BLEND
title: D2D1_BLEND (d2d1effectauthor.h)
description: Specifies how one of the color sources is to be derived and optionally specifies a preblend operation on the color source.
helpviewer_keywords: ["D2D1_BLEND","D2D1_BLEND enumeration [Direct2D]","D2D1_BLEND_BLEND_FACTOR","D2D1_BLEND_DEST_ALPHA","D2D1_BLEND_DEST_COLOR","D2D1_BLEND_INV_BLEND_FACTOR","D2D1_BLEND_INV_DEST_ALPHA","D2D1_BLEND_INV_DEST_COLOR","D2D1_BLEND_INV_SRC_ALPHA","D2D1_BLEND_INV_SRC_COLOR","D2D1_BLEND_ONE","D2D1_BLEND_SRC_ALPHA","D2D1_BLEND_SRC_ALPHA_SAT","D2D1_BLEND_SRC_COLOR","D2D1_BLEND_ZERO","d2d1effectauthor/D2D1_BLEND","d2d1effectauthor/D2D1_BLEND_BLEND_FACTOR","d2d1effectauthor/D2D1_BLEND_DEST_ALPHA","d2d1effectauthor/D2D1_BLEND_DEST_COLOR","d2d1effectauthor/D2D1_BLEND_INV_BLEND_FACTOR","d2d1effectauthor/D2D1_BLEND_INV_DEST_ALPHA","d2d1effectauthor/D2D1_BLEND_INV_DEST_COLOR","d2d1effectauthor/D2D1_BLEND_INV_SRC_ALPHA","d2d1effectauthor/D2D1_BLEND_INV_SRC_COLOR","d2d1effectauthor/D2D1_BLEND_ONE","d2d1effectauthor/D2D1_BLEND_SRC_ALPHA","d2d1effectauthor/D2D1_BLEND_SRC_ALPHA_SAT","d2d1effectauthor/D2D1_BLEND_SRC_COLOR","d2d1effectauthor/D2D1_BLEND_ZERO","direct2d.d2d1_blend"]
old-location: direct2d\d2d1_blend.htm
tech.root: Direct2D
ms.assetid: 9bc91efd-f695-4bc6-a63e-a3862cca91dd
ms.date: 12/05/2018
ms.keywords: D2D1_BLEND, D2D1_BLEND enumeration [Direct2D], D2D1_BLEND_BLEND_FACTOR, D2D1_BLEND_DEST_ALPHA, D2D1_BLEND_DEST_COLOR, D2D1_BLEND_INV_BLEND_FACTOR, D2D1_BLEND_INV_DEST_ALPHA, D2D1_BLEND_INV_DEST_COLOR, D2D1_BLEND_INV_SRC_ALPHA, D2D1_BLEND_INV_SRC_COLOR, D2D1_BLEND_ONE, D2D1_BLEND_SRC_ALPHA, D2D1_BLEND_SRC_ALPHA_SAT, D2D1_BLEND_SRC_COLOR, D2D1_BLEND_ZERO, d2d1effectauthor/D2D1_BLEND, d2d1effectauthor/D2D1_BLEND_BLEND_FACTOR, d2d1effectauthor/D2D1_BLEND_DEST_ALPHA, d2d1effectauthor/D2D1_BLEND_DEST_COLOR, d2d1effectauthor/D2D1_BLEND_INV_BLEND_FACTOR, d2d1effectauthor/D2D1_BLEND_INV_DEST_ALPHA, d2d1effectauthor/D2D1_BLEND_INV_DEST_COLOR, d2d1effectauthor/D2D1_BLEND_INV_SRC_ALPHA, d2d1effectauthor/D2D1_BLEND_INV_SRC_COLOR, d2d1effectauthor/D2D1_BLEND_ONE, d2d1effectauthor/D2D1_BLEND_SRC_ALPHA, d2d1effectauthor/D2D1_BLEND_SRC_ALPHA_SAT, d2d1effectauthor/D2D1_BLEND_SRC_COLOR, d2d1effectauthor/D2D1_BLEND_ZERO, direct2d.d2d1_blend
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1effectauthor.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_BLEND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BLEND
 - d2d1effectauthor/D2D1_BLEND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - d2d1effectauthor.lib
api_name:
 - D2D1_BLEND
---

# D2D1_BLEND enumeration


## -description

Specifies how one of the color sources is to be derived and optionally specifies a preblend operation on the color source.

## -enum-fields

### -field D2D1_BLEND_ZERO:1

The data source is black (0, 0, 0, 0). There is no preblend operation.

### -field D2D1_BLEND_ONE:2

The data source is white (1, 1, 1, 1). There is no preblend operation.

### -field D2D1_BLEND_SRC_COLOR:3

The data source is color data (RGB) from the second input of the blend transform. There is not a preblend operation.

### -field D2D1_BLEND_INV_SRC_COLOR:4

The data source is color data (RGB) from second input of the blend transform. The preblend operation inverts the data, generating 1 - RGB.

### -field D2D1_BLEND_SRC_ALPHA:5

The data source is alpha data (A) from second input of the blend transform. There is no preblend operation.

### -field D2D1_BLEND_INV_SRC_ALPHA:6

The data source is alpha data (A) from the second input of the blend transform. The preblend operation inverts the data, generating 1 - A.

### -field D2D1_BLEND_DEST_ALPHA:7

The data source is alpha data (A) from the first input of the blend transform. There is no preblend operation.

### -field D2D1_BLEND_INV_DEST_ALPHA:8

The data source is alpha data (A) from the first input of the blend transform. The preblend operation inverts the data, generating 1 - A.

### -field D2D1_BLEND_DEST_COLOR:9

The data source is color data from the first input of the blend transform. There is no preblend operation.

### -field D2D1_BLEND_INV_DEST_COLOR:10

The data source is color data from the first input of the blend transform. The preblend operation inverts the data, generating 1 - RGB.

### -field D2D1_BLEND_SRC_ALPHA_SAT:11

The data source is alpha data from the second input of the blend transform. The preblend operation clamps the data to 1 or less.

### -field D2D1_BLEND_BLEND_FACTOR:14

The data source is the blend factor. There is no preblend operation.

### -field D2D1_BLEND_INV_BLEND_FACTOR:15

The data source is the blend factor. The preblend operation inverts the blend factor, generating 1 - blend_factor.

### -field D2D1_BLEND_FORCE_DWORD:0xffffffff

## -remarks

This enumeration has the same numeric values as <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend">D3D10_BLEND</a>.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description">D2D1_BLEND_DESCRIPTION</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform">ID2D1BlendTransform</a>
