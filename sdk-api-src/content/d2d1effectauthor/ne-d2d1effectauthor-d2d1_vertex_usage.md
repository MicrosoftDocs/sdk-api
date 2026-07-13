---
UID: NE:d2d1effectauthor.D2D1_VERTEX_USAGE
title: D2D1_VERTEX_USAGE (d2d1effectauthor.h)
description: Indicates whether the vertex buffer changes infrequently or frequently.
helpviewer_keywords: ["D2D1_VERTEX_USAGE","D2D1_VERTEX_USAGE enumeration [Direct2D]","D2D1_VERTEX_USAGE_DYNAMIC","D2D1_VERTEX_USAGE_STATIC","d2d1effectauthor/D2D1_VERTEX_USAGE","d2d1effectauthor/D2D1_VERTEX_USAGE_DYNAMIC","d2d1effectauthor/D2D1_VERTEX_USAGE_STATIC","direct2d.d2d1_vertex_usage"]
old-location: direct2d\d2d1_vertex_usage.htm
tech.root: Direct2D
ms.assetid: ff122e0d-5f0e-4a61-bead-53bea6f1648f
ms.date: 12/05/2018
ms.keywords: D2D1_VERTEX_USAGE, D2D1_VERTEX_USAGE enumeration [Direct2D], D2D1_VERTEX_USAGE_DYNAMIC, D2D1_VERTEX_USAGE_STATIC, d2d1effectauthor/D2D1_VERTEX_USAGE, d2d1effectauthor/D2D1_VERTEX_USAGE_DYNAMIC, d2d1effectauthor/D2D1_VERTEX_USAGE_STATIC, direct2d.d2d1_vertex_usage
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
req.typenames: D2D1_VERTEX_USAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_VERTEX_USAGE
 - d2d1effectauthor/D2D1_VERTEX_USAGE
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
 - D2D1_VERTEX_USAGE
---

# D2D1_VERTEX_USAGE enumeration


## -description

Indicates whether the vertex buffer changes infrequently or frequently.

## -enum-fields

### -field D2D1_VERTEX_USAGE_STATIC:0

The created vertex buffer is updated infrequently.

### -field D2D1_VERTEX_USAGE_DYNAMIC:1

The created vertex buffer is changed frequently.

### -field D2D1_VERTEX_USAGE_FORCE_DWORD:0xffffffff

## -remarks

If a dynamic vertex buffer is created, Direct2D will not necessarily map the buffer directly to a Direct3D vertex buffer. Instead, a system memory copy can be copied to the rendering engine vertex buffer as the effects are rendered.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description">D2D1_BLEND_DESCRIPTION</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform">ID2D1BlendTransform</a>
