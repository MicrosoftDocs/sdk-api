---
UID: NF:d2d1.ID2D1RadialGradientBrush.GetGradientStopCollection
title: ID2D1RadialGradientBrush::GetGradientStopCollection (d2d1.h)
description: Retrieves the ID2D1GradientStopCollection associated with this radial gradient brush object.
helpviewer_keywords: ["GetGradientStopCollection","GetGradientStopCollection method [Direct2D]","GetGradientStopCollection method [Direct2D]","ID2D1RadialGradientBrush interface","ID2D1RadialGradientBrush interface [Direct2D]","GetGradientStopCollection method","ID2D1RadialGradientBrush.GetGradientStopCollection","ID2D1RadialGradientBrush::GetGradientStopCollection","d2d1/ID2D1RadialGradientBrush::GetGradientStopCollection","direct2d.ID2D1RadialGradientBrush_GetGradientStopCollection"]
old-location: direct2d\ID2D1RadialGradientBrush_GetGradientStopCollection.htm
tech.root: Direct2D
ms.assetid: e09a7b3d-4c37-4d39-985f-a24a3bfe2d04
ms.date: 12/05/2018
ms.keywords: GetGradientStopCollection, GetGradientStopCollection method [Direct2D], GetGradientStopCollection method [Direct2D],ID2D1RadialGradientBrush interface, ID2D1RadialGradientBrush interface [Direct2D],GetGradientStopCollection method, ID2D1RadialGradientBrush.GetGradientStopCollection, ID2D1RadialGradientBrush::GetGradientStopCollection, d2d1/ID2D1RadialGradientBrush::GetGradientStopCollection, direct2d.ID2D1RadialGradientBrush_GetGradientStopCollection
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1RadialGradientBrush::GetGradientStopCollection
 - d2d1/ID2D1RadialGradientBrush::GetGradientStopCollection
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
 - ID2D1RadialGradientBrush.GetGradientStopCollection
---

# ID2D1RadialGradientBrush::GetGradientStopCollection


## -description

Retrieves the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a> associated with this radial gradient brush object.

## -parameters

### -param gradientStopCollection [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>**</b>

The  <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a> object associated with this linear gradient brush object. This parameter is passed uninitialized.

## -remarks

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a> contains an array of <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> structures and additional information, such as the extend mode and the color interpolation mode.

## -see-also

<a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>

