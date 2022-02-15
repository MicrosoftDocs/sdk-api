---
UID: NE:d2d1_3.D2D1_SPRITE_OPTIONS
title: D2D1_SPRITE_OPTIONS (d2d1_3.h)
description: Specifies additional aspects of how a sprite batch is to be drawn, as part of a call to ID2D1DeviceContext3::DrawSpriteBatch.
helpviewer_keywords: ["D2D1_SPRITE_OPTIONS","D2D1_SPRITE_OPTIONS enumeration [Direct2D]","D2D1_SPRITE_OPTIONS_CLAMP_TO_SOURCE_RECTANGLE","D2D1_SPRITE_OPTIONS_NONE","d2d1_3/D2D1_SPRITE_OPTIONS","d2d1_3/D2D1_SPRITE_OPTIONS_CLAMP_TO_SOURCE_RECTANGLE","d2d1_3/D2D1_SPRITE_OPTIONS_NONE","direct2d.d2d1_sprite_options"]
old-location: direct2d\d2d1_sprite_options.htm
tech.root: Direct2D
ms.assetid: 64B7D987-A79C-412C-8D12-53E21DD8DDD9
ms.date: 12/05/2018
ms.keywords: D2D1_SPRITE_OPTIONS, D2D1_SPRITE_OPTIONS enumeration [Direct2D], D2D1_SPRITE_OPTIONS_CLAMP_TO_SOURCE_RECTANGLE, D2D1_SPRITE_OPTIONS_NONE, d2d1_3/D2D1_SPRITE_OPTIONS, d2d1_3/D2D1_SPRITE_OPTIONS_CLAMP_TO_SOURCE_RECTANGLE, d2d1_3/D2D1_SPRITE_OPTIONS_NONE, direct2d.d2d1_sprite_options
req.header: d2d1_3.h
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
req.typenames: D2D1_SPRITE_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SPRITE_OPTIONS
 - d2d1_3/D2D1_SPRITE_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_3.h
api_name:
 - D2D1_SPRITE_OPTIONS
---

# D2D1_SPRITE_OPTIONS enumeration


## -description

Specifies additional aspects of how a sprite batch is to be drawn, as part of a call to <a href="/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options)">ID2D1DeviceContext3::DrawSpriteBatch</a>.

## -enum-fields

### -field D2D1_SPRITE_OPTIONS_NONE:0

Default value. No special drawing configuration. This option yields the best drawing performance.

### -field D2D1_SPRITE_OPTIONS_CLAMP_TO_SOURCE_RECTANGLE:1

Interpolation of bitmap pixels will be clamped to the sprite’s source rectangle. 
          If the sub-images in your source bitmap have no pixels separating them, then you may see color bleeding when drawing them with D2D1_SPRITE_OPTIONS_NONE. 
          In that case, consider adding borders between them with your sprite-packing tool, or use this option.
          Note that drawing sprites with this option enabled is slower than using D2D1_SPRITE_OPTIONS_NONE.

### -field D2D1_SPRITE_OPTIONS_FORCE_DWORD:0xffffffff

