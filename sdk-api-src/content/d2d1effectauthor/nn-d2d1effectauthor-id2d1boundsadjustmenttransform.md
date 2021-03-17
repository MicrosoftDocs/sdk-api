---
UID: NN:d2d1effectauthor.ID2D1BoundsAdjustmentTransform
title: ID2D1BoundsAdjustmentTransform (d2d1effectauthor.h)
description: A support transform for effects to modify the output rectangle of the previous effect or bitmap.
helpviewer_keywords: ["ID2D1BoundsAdjustmentTransform","ID2D1BoundsAdjustmentTransform interface [Direct2D]","ID2D1BoundsAdjustmentTransform interface [Direct2D]","described","d2d1effectauthor/ID2D1BoundsAdjustmentTransform","direct2d.id2d1boundadjustmenttransform"]
old-location: direct2d\id2d1boundadjustmenttransform.htm
tech.root: Direct2D
ms.assetid: 40482670-2989-47B2-9558-FF017C8A2FBB
ms.date: 12/05/2018
ms.keywords: ID2D1BoundsAdjustmentTransform, ID2D1BoundsAdjustmentTransform interface [Direct2D], ID2D1BoundsAdjustmentTransform interface [Direct2D],described, d2d1effectauthor/ID2D1BoundsAdjustmentTransform, direct2d.id2d1boundadjustmenttransform
req.header: d2d1effectauthor.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1BoundsAdjustmentTransform
 - d2d1effectauthor/ID2D1BoundsAdjustmentTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1effectauthor.h
api_name:
 - ID2D1BoundsAdjustmentTransform
---

## -description

A support transform for effects to modify the output rectangle of the previous effect or bitmap.

## -inheritance

The **ID2D1BoundsAdjustmentTransform** interface inherits from the [ID2D1TransformNode](./nn-d2d1effectauthor-id2d1transformnode.md) interface.

## -remarks

The support transform can be used for two different reasons.

<ul>
<li>
To indicate that a region of its input image is already transparent black.  The expanded area will be treated as transparent black.

This can increase efficiency for rendering bitmaps.

</li>
<li>
To increase the size of the input image.

</li>
</ul>