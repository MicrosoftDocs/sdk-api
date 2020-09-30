---
UID: NF:d2d1_1.ID2D1BitmapBrush1.SetInterpolationMode1
title: ID2D1BitmapBrush1::SetInterpolationMode1 (d2d1_1.h)
description: Sets the interpolation mode for the brush.
helpviewer_keywords: ["ID2D1BitmapBrush1 interface [Direct2D]","SetInterpolationMode1 method","ID2D1BitmapBrush1.SetInterpolationMode1","ID2D1BitmapBrush1::SetInterpolationMode1","SetInterpolationMode1","SetInterpolationMode1 method [Direct2D]","SetInterpolationMode1 method [Direct2D]","ID2D1BitmapBrush1 interface","d2d1_1/ID2D1BitmapBrush1::SetInterpolationMode1","direct2d.id2d1bitmapbrush1_setinterpolationmode1"]
old-location: direct2d\id2d1bitmapbrush1_setinterpolationmode1.htm
tech.root: Direct2D
ms.assetid: 55CBCA8D-5155-4D26-B868-41571A2DB640
ms.date: 12/05/2018
ms.keywords: ID2D1BitmapBrush1 interface [Direct2D],SetInterpolationMode1 method, ID2D1BitmapBrush1.SetInterpolationMode1, ID2D1BitmapBrush1::SetInterpolationMode1, SetInterpolationMode1, SetInterpolationMode1 method [Direct2D], SetInterpolationMode1 method [Direct2D],ID2D1BitmapBrush1 interface, d2d1_1/ID2D1BitmapBrush1::SetInterpolationMode1, direct2d.id2d1bitmapbrush1_setinterpolationmode1
req.header: d2d1_1.h
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
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1BitmapBrush1::SetInterpolationMode1
 - d2d1_1/ID2D1BitmapBrush1::SetInterpolationMode1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1BitmapBrush1.SetInterpolationMode1
---

# ID2D1BitmapBrush1::SetInterpolationMode1


## -description

Sets the interpolation mode for the brush.

## -parameters

### -param interpolationMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode">D2D1_INTERPOLATION_MODE</a></b>

The mode to use.

## -returns

<div class="alert"><b>Note</b>  If <i>interpolationMode</i> is not a valid member of D2D1_INTERPOLATION_MODE, then this method silently ignores the call.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1">ID2D1BitmapBrush1</a>