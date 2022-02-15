---
UID: NE:d2d1.D2D1_ANTIALIAS_MODE
title: D2D1_ANTIALIAS_MODE (d2d1.h)
description: Specifies how the edges of nontext primitives are rendered.
helpviewer_keywords: ["D2D1_ANTIALIAS_MODE","D2D1_ANTIALIAS_MODE enumeration [Direct2D]","D2D1_ANTIALIAS_MODE_ALIASED","D2D1_ANTIALIAS_MODE_PER_PRIMITIVE","d2d1/D2D1_ANTIALIAS_MODE","d2d1/D2D1_ANTIALIAS_MODE_ALIASED","d2d1/D2D1_ANTIALIAS_MODE_PER_PRIMITIVE","direct2d.D2D1_ANTIALIAS_MODE"]
old-location: direct2d\D2D1_ANTIALIAS_MODE.htm
tech.root: Direct2D
ms.assetid: 3ca12155-6dd0-41bb-8778-3387422c4ffe
ms.date: 12/05/2018
ms.keywords: D2D1_ANTIALIAS_MODE, D2D1_ANTIALIAS_MODE enumeration [Direct2D], D2D1_ANTIALIAS_MODE_ALIASED, D2D1_ANTIALIAS_MODE_PER_PRIMITIVE, d2d1/D2D1_ANTIALIAS_MODE, d2d1/D2D1_ANTIALIAS_MODE_ALIASED, d2d1/D2D1_ANTIALIAS_MODE_PER_PRIMITIVE, direct2d.D2D1_ANTIALIAS_MODE
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: D2D1_ANTIALIAS_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_ANTIALIAS_MODE
 - d2d1/D2D1_ANTIALIAS_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_ANTIALIAS_MODE
---

# D2D1_ANTIALIAS_MODE enumeration


## -description

Specifies how the edges of nontext primitives are rendered.

## -enum-fields

### -field D2D1_ANTIALIAS_MODE_PER_PRIMITIVE:0

Edges are antialiased using the Direct2D per-primitive method of high-quality antialiasing.

### -field D2D1_ANTIALIAS_MODE_ALIASED:1

Objects are aliased in most cases. Objects are antialiased only when they are drawn to a render target created by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)">CreateDxgiSurfaceRenderTarget</a> method and  Direct3D multisampling has been enabled on the backing DirectX Graphics Infrastructure (DXGI) surface.

### -field D2D1_ANTIALIAS_MODE_FORCE_DWORD:0xffffffff

