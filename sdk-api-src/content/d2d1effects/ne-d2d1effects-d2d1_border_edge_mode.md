---
UID: NE:d2d1effects.D2D1_BORDER_EDGE_MODE
title: D2D1_BORDER_EDGE_MODE (d2d1effects.h)
description: The edge mode for the Border effect.
helpviewer_keywords: ["D2D1_BORDER_EDGE_MODE","D2D1_BORDER_EDGE_MODE enumeration [Direct2D]","D2D1_BORDER_EDGE_MODE_CLAMP","D2D1_BORDER_EDGE_MODE_MIRROR","D2D1_BORDER_EDGE_MODE_WRAP","d2d1effects/D2D1_BORDER_EDGE_MODE","d2d1effects/D2D1_BORDER_EDGE_MODE_CLAMP","d2d1effects/D2D1_BORDER_EDGE_MODE_MIRROR","d2d1effects/D2D1_BORDER_EDGE_MODE_WRAP","direct2d.d2d1_border_edge_mode"]
old-location: direct2d\d2d1_border_edge_mode.htm
tech.root: Direct2D
ms.assetid: CAB73FFA-2F81-467F-8A4D-D523793BF659
ms.date: 12/05/2018
ms.keywords: D2D1_BORDER_EDGE_MODE, D2D1_BORDER_EDGE_MODE enumeration [Direct2D], D2D1_BORDER_EDGE_MODE_CLAMP, D2D1_BORDER_EDGE_MODE_MIRROR, D2D1_BORDER_EDGE_MODE_WRAP, d2d1effects/D2D1_BORDER_EDGE_MODE, d2d1effects/D2D1_BORDER_EDGE_MODE_CLAMP, d2d1effects/D2D1_BORDER_EDGE_MODE_MIRROR, d2d1effects/D2D1_BORDER_EDGE_MODE_WRAP, direct2d.d2d1_border_edge_mode
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
req.typenames: D2D1_BORDER_EDGE_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BORDER_EDGE_MODE
 - d2d1effects/D2D1_BORDER_EDGE_MODE
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
 - D2D1_BORDER_EDGE_MODE
---

# D2D1_BORDER_EDGE_MODE enumeration


## -description

The edge mode for the <a href="/windows/desktop/Direct2D/border">Border effect</a>.

## -enum-fields

### -field D2D1_BORDER_EDGE_MODE_CLAMP:0

Repeats the pixels from the edges of the image.

### -field D2D1_BORDER_EDGE_MODE_WRAP:1

Uses pixels from the opposite end edge of the image.

### -field D2D1_BORDER_EDGE_MODE_MIRROR:2

Reflects pixels about the edge of the image.

### -field D2D1_BORDER_EDGE_MODE_FORCE_DWORD:0xffffffff
