---
UID: NE:d2d1effects.D2D1_TILE_PROP
title: D2D1_TILE_PROP (d2d1effects.h)
description: Identifiers for properties of the Tile effect.
helpviewer_keywords: ["D2D1_TILE_PROP","D2D1_TILE_PROP enumeration [Direct2D]","D2D1_TILE_PROP_RECT","d2d1effects/D2D1_TILE_PROP","d2d1effects/D2D1_TILE_PROP_RECT","direct2d.d2d1_tile_prop"]
old-location: direct2d\d2d1_tile_prop.htm
tech.root: Direct2D
ms.assetid: F5A1A309-1844-4C8A-8F6F-0E2D82CB4AFD
ms.date: 12/05/2018
ms.keywords: D2D1_TILE_PROP, D2D1_TILE_PROP enumeration [Direct2D], D2D1_TILE_PROP_RECT, d2d1effects/D2D1_TILE_PROP, d2d1effects/D2D1_TILE_PROP_RECT, direct2d.d2d1_tile_prop
req.header: d2d1effects.h
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
req.typenames: D2D1_TILE_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_TILE_PROP
 - d2d1effects/D2D1_TILE_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_TILE_PROP
---

# D2D1_TILE_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/tile">Tile effect</a>.

## -enum-fields

### -field D2D1_TILE_PROP_RECT:0

The region of the image to be tiled. This property is a <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f">D2D1_VECTOR_4F</a> defined as: (left, top, right, bottom). The units are in DIPs.
            

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f">D2D1_VECTOR_4F</a>.

The default is {0.0f, 0.0f, 100.0f, 100.0f}.

### -field D2D1_TILE_PROP_FORCE_DWORD:0xffffffff
