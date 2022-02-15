---
UID: NE:d2d1.D2D1_OPACITY_MASK_CONTENT
title: D2D1_OPACITY_MASK_CONTENT (d2d1.h)
description: Describes whether an opacity mask contains graphics or text. Direct2D uses this information to determine which gamma space to use when blending the opacity mask.
helpviewer_keywords: ["D2D1_OPACITY_MASK_CONTENT","D2D1_OPACITY_MASK_CONTENT enumeration [Direct2D]","D2D1_OPACITY_MASK_CONTENT_GRAPHICS","D2D1_OPACITY_MASK_CONTENT_TEXT_GDI_COMPATIBLE","D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL","d2d1/D2D1_OPACITY_MASK_CONTENT","d2d1/D2D1_OPACITY_MASK_CONTENT_GRAPHICS","d2d1/D2D1_OPACITY_MASK_CONTENT_TEXT_GDI_COMPATIBLE","d2d1/D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL","direct2d.d2d1_opacity_mask_content"]
old-location: direct2d\d2d1_opacity_mask_content.htm
tech.root: Direct2D
ms.assetid: ea14d7eb-b8cc-4ab8-8f51-9174748ee6a2
ms.date: 12/05/2018
ms.keywords: D2D1_OPACITY_MASK_CONTENT, D2D1_OPACITY_MASK_CONTENT enumeration [Direct2D], D2D1_OPACITY_MASK_CONTENT_GRAPHICS, D2D1_OPACITY_MASK_CONTENT_TEXT_GDI_COMPATIBLE, D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL, d2d1/D2D1_OPACITY_MASK_CONTENT, d2d1/D2D1_OPACITY_MASK_CONTENT_GRAPHICS, d2d1/D2D1_OPACITY_MASK_CONTENT_TEXT_GDI_COMPATIBLE, d2d1/D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL, direct2d.d2d1_opacity_mask_content
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
req.typenames: D2D1_OPACITY_MASK_CONTENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_OPACITY_MASK_CONTENT
 - d2d1/D2D1_OPACITY_MASK_CONTENT
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
 - D2D1_OPACITY_MASK_CONTENT
---

# D2D1_OPACITY_MASK_CONTENT enumeration


## -description

Describes whether an opacity mask contains graphics or text. Direct2D uses this information to determine which gamma space to use when blending the opacity mask.

## -enum-fields

### -field D2D1_OPACITY_MASK_CONTENT_GRAPHICS:0

The opacity mask contains graphics. The opacity mask is blended in the gamma 2.2 color space.

### -field D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL:1

The opacity mask contains non-GDI text. The gamma space used for blending is obtained from the render target's text rendering parameters. (<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams">ID2D1RenderTarget::SetTextRenderingParams</a>).

### -field D2D1_OPACITY_MASK_CONTENT_TEXT_GDI_COMPATIBLE:2

The opacity mask contains text rendered using the GDI-compatible rendering mode. The opacity mask is blended using the gamma for GDI rendering.

### -field D2D1_OPACITY_MASK_CONTENT_FORCE_DWORD:0xffffffff

## -see-also

<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)">FillOpacityMask</a>

