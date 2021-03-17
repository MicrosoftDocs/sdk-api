---
UID: NS:d2d1_3.D2D1_INK_POINT
title: D2D1_INK_POINT (d2d1_3.h)
description: Represents a point, radius pair that makes up part of a D2D1_INK_BEZIER_SEGMENT.
helpviewer_keywords: ["D2D1_INK_POINT","D2D1_INK_POINT structure [Direct2D]","d2d1_3/D2D1_INK_POINT","direct2d.d2d1_ink_point"]
old-location: direct2d\d2d1_ink_point.htm
tech.root: Direct2D
ms.assetid: C18E7B04-12B8-4EB9-BAFB-24FBA99210E9
ms.date: 12/05/2018
ms.keywords: D2D1_INK_POINT, D2D1_INK_POINT structure [Direct2D], d2d1_3/D2D1_INK_POINT, direct2d.d2d1_ink_point
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
req.typenames: D2D1_INK_POINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_INK_POINT
 - d2d1_3/D2D1_INK_POINT
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
 - D2D1_INK_POINT
---

# D2D1_INK_POINT structure


## -description

Represents a point, radius pair that makes up part of a <a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment">D2D1_INK_BEZIER_SEGMENT</a>.

## -struct-fields

### -field x

The x-coordinate of the point.

### -field y

The y-coordinate of the point.

### -field radius

The radius of this point. Corresponds to the width of the ink stroke at this point in the stroke.