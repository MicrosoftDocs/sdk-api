---
UID: NF:d2d1helper.GradientStop
title: GradientStop function (d2d1helper.h)
description: Creates a D2D1_GRADIENT_STOP structure.
helpviewer_keywords: ["GradientStop","GradientStop function [Direct2D]","d2d1helper/GradientStop","direct2d.gradientstop"]
old-location: direct2d\gradientstop.htm
tech.root: Direct2D
ms.assetid: 37f413e8-36ee-462d-8419-908690094c49
ms.date: 12/05/2018
ms.keywords: GradientStop, GradientStop function [Direct2D], d2d1helper/GradientStop, direct2d.gradientstop
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
 - GradientStop
 - d2d1helper/GradientStop
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
 - GradientStop
---

# GradientStop function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> structure.

## -parameters

### -param position

Type: <b>FLOAT</b>

A value that indicates the relative position of the gradient stop in the brush. A value of 0.0 specifies that the stop is positioned at the beginning of the gradient vector, while a value of 1.0 specifies that the stop is positioned at the end of the gradient vector. Stops outside the 0.0-1.0 range might not be directly visible but still influence the gradient pattern.

### -param color [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-color-f">D2D1_COLOR_F</a></b>

The color of the gradient stop.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a></b>

The new gradient stop.

## -see-also

<a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>