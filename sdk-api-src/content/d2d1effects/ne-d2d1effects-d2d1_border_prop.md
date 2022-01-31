---
UID: NE:d2d1effects.D2D1_BORDER_PROP
title: D2D1_BORDER_PROP (d2d1effects.h)
description: Identifiers for properties of the Border effect.
helpviewer_keywords: ["D2D1_BORDER_PROP","D2D1_BORDER_PROP enumeration [Direct2D]","D2D1_BORDER_PROP_EDGE_MODE_X","D2D1_BORDER_PROP_EDGE_MODE_Y","d2d1effects/D2D1_BORDER_PROP","d2d1effects/D2D1_BORDER_PROP_EDGE_MODE_X","d2d1effects/D2D1_BORDER_PROP_EDGE_MODE_Y","direct2d.d2d1_border_prop"]
old-location: direct2d\d2d1_border_prop.htm
tech.root: Direct2D
ms.assetid: A8622A21-4B06-4262-B68C-A4FF075CFF37
ms.date: 12/05/2018
ms.keywords: D2D1_BORDER_PROP, D2D1_BORDER_PROP enumeration [Direct2D], D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_PROP_EDGE_MODE_Y, d2d1effects/D2D1_BORDER_PROP, d2d1effects/D2D1_BORDER_PROP_EDGE_MODE_X, d2d1effects/D2D1_BORDER_PROP_EDGE_MODE_Y, direct2d.d2d1_border_prop
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
req.typenames: D2D1_BORDER_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BORDER_PROP
 - d2d1effects/D2D1_BORDER_PROP
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
 - D2D1_BORDER_PROP
---

# D2D1_BORDER_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/border">Border effect</a>.

## -enum-fields

### -field D2D1_BORDER_PROP_EDGE_MODE_X:0

The edge mode in the X direction for the effect. You can set this to clamp, wrap, or mirror.
            

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_border_edge_mode">D2D1_BORDER_EDGE_MODE</a>.

The default value is D2D1_BORDER_EDGE_MODE_CLAMP.

### -field D2D1_BORDER_PROP_EDGE_MODE_Y:1

The edge mode in the Y direction for the effect. You can set this to clamp, wrap, or mirror.
            

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_border_edge_mode">D2D1_BORDER_EDGE_MODE</a>.

The default value is D2D1_BORDER_EDGE_MODE_CLAMP.

### -field D2D1_BORDER_PROP_FORCE_DWORD:0xffffffff
