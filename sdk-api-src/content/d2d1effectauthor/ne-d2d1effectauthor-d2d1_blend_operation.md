---
UID: NE:d2d1effectauthor.D2D1_BLEND_OPERATION
title: D2D1_BLEND_OPERATION (d2d1effectauthor.h)
description: Specifies the blend operation on two color sources.
helpviewer_keywords: ["D2D1_BLEND_OPERATION","D2D1_BLEND_OPERATION enumeration [Direct2D]","D2D1_BLEND_OPERATION_ADD","D2D1_BLEND_OPERATION_MAX","D2D1_BLEND_OPERATION_MIN","D2D1_BLEND_OPERATION_REV_SUBSTRACT","D2D1_BLEND_OPERATION_SUBTRACT","d2d1effectauthor/D2D1_BLEND_OPERATION","d2d1effectauthor/D2D1_BLEND_OPERATION_ADD","d2d1effectauthor/D2D1_BLEND_OPERATION_MAX","d2d1effectauthor/D2D1_BLEND_OPERATION_MIN","d2d1effectauthor/D2D1_BLEND_OPERATION_REV_SUBSTRACT","d2d1effectauthor/D2D1_BLEND_OPERATION_SUBTRACT","direct2d.d2d1_blend_operation"]
old-location: direct2d\d2d1_blend_operation.htm
tech.root: Direct2D
ms.assetid: 54977cf3-cca3-4a1e-a039-1ee4a8d44686
ms.date: 12/05/2018
ms.keywords: D2D1_BLEND_OPERATION, D2D1_BLEND_OPERATION enumeration [Direct2D], D2D1_BLEND_OPERATION_ADD, D2D1_BLEND_OPERATION_MAX, D2D1_BLEND_OPERATION_MIN, D2D1_BLEND_OPERATION_REV_SUBSTRACT, D2D1_BLEND_OPERATION_SUBTRACT, d2d1effectauthor/D2D1_BLEND_OPERATION, d2d1effectauthor/D2D1_BLEND_OPERATION_ADD, d2d1effectauthor/D2D1_BLEND_OPERATION_MAX, d2d1effectauthor/D2D1_BLEND_OPERATION_MIN, d2d1effectauthor/D2D1_BLEND_OPERATION_REV_SUBSTRACT, d2d1effectauthor/D2D1_BLEND_OPERATION_SUBTRACT, direct2d.d2d1_blend_operation
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
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_BLEND_OPERATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BLEND_OPERATION
 - d2d1effectauthor/D2D1_BLEND_OPERATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_BLEND_OPERATION
---

## -description

Specifies the blend operation on two color sources.

## -enum-fields

### -field D2D1_BLEND_OPERATION_ADD:1

Add source 1 and source 2.

### -field D2D1_BLEND_OPERATION_SUBTRACT:2

Subtract source 1 from source 2.

### -field D2D1_BLEND_OPERATION_REV_SUBTRACT:3

Subtract source 2 from source 1.

### -field D2D1_BLEND_OPERATION_MIN:4

Find the minimum of source 1 and source 2.

### -field D2D1_BLEND_OPERATION_MAX:5

Find the maximum of source 1 and source 2.

### -field D2D1_BLEND_OPERATION_FORCE_DWORD:0xffffffff

A value guaranteed to be a DWORD.

## -remarks

This enumeration has the same numeric values as <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_blend_op">D3D10_BLEND_OP</a>.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description">D2D1_BLEND_DESCRIPTION</a>

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform">ID2D1BlendTransform</a>
