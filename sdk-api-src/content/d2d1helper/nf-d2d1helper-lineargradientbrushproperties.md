---
UID: NF:d2d1helper.LinearGradientBrushProperties
title: LinearGradientBrushProperties function (d2d1helper.h)
description: Creates a D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES structure.
helpviewer_keywords: ["LinearGradientBrushProperties","LinearGradientBrushProperties function [Direct2D]","d2d1helper/LinearGradientBrushProperties","direct2d.lineargradientbrushproperties"]
old-location: direct2d\lineargradientbrushproperties.htm
tech.root: Direct2D
ms.assetid: dba59936-2b2d-4a9b-aba4-acb6ff84c037
ms.date: 12/05/2018
ms.keywords: LinearGradientBrushProperties, LinearGradientBrushProperties function [Direct2D], d2d1helper/LinearGradientBrushProperties, direct2d.lineargradientbrushproperties
req.header: d2d1helper.h
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
 - LinearGradientBrushProperties
 - d2d1helper/LinearGradientBrushProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - LinearGradientBrushProperties
---

# LinearGradientBrushProperties function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties">D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES</a> structure.

## -parameters

### -param startPoint [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The start point, in the brush's coordinate space, of the gradient axis.

### -param endPoint [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The end point, in the brush's coordinate space, of the gradient axis.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties">D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES</a></b>

A structure that contains the start and end point of the gradient axis for an <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a>.