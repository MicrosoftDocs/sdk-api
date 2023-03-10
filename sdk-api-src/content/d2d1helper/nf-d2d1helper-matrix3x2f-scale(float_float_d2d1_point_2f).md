---
UID: NF:d2d1helper.Matrix3x2F.Scale(FLOAT,FLOAT,D2D1_POINT_2F)
title: Matrix3x2F::Scale(FLOAT,FLOAT,D2D1_POINT_2F) (d2d1helper.h)
description: Creates a scale transformation that has the specified scale factors and center point. (overload 1/2)
helpviewer_keywords: ["D2D1.Matrix3x2F.Scale","D2D1::Matrix3x2F::Scale","Matrix3x2F interface [Direct2D]","Scale method","Matrix3x2F.Scale","Matrix3x2F.Scale(FLOAT","FLOAT","D2D1_POINT_2F)","Matrix3x2F::Scale","Matrix3x2F::Scale(FLOAT","FLOAT","D2D1_POINT_2F)","Scale","Scale method [Direct2D]","Scale method [Direct2D]","Matrix3x2F interface","d2d1helper/Matrix3x2F::Scale","direct2d.matrix3x2f_scale_float_float_d2d1_point_2f_"]
old-location: direct2d\matrix3x2f_scale_float_float_d2d1_point_2f_.htm
tech.root: Direct2D
ms.assetid: 401b8710-c486-44b0-b79c-d7238279fdef
ms.date: 12/05/2018
ms.keywords: D2D1.Matrix3x2F.Scale, D2D1::Matrix3x2F::Scale, Matrix3x2F interface [Direct2D],Scale method, Matrix3x2F.Scale, Matrix3x2F.Scale(FLOAT,FLOAT,D2D1_POINT_2F), Matrix3x2F::Scale, Matrix3x2F::Scale(FLOAT,FLOAT,D2D1_POINT_2F), Scale, Scale method [Direct2D], Scale method [Direct2D],Matrix3x2F interface, d2d1helper/Matrix3x2F::Scale, direct2d.matrix3x2f_scale_float_float_d2d1_point_2f_
req.header: d2d1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: D2D1
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
 - Matrix3x2F::Scale
 - d2d1helper/Matrix3x2F::Scale
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
 - Matrix3x2F.Scale
---

# Matrix3x2F::Scale(FLOAT,FLOAT,D2D1_POINT_2F)


## -description

Creates a scale transformation that has the specified scale factors and center point.

## -parameters

### -param x

Type: <b>FLOAT</b>

The x-axis scale factor of the scale transformation.

### -param y

Type: <b>FLOAT</b>

The y-axis scale factor of the scale transformation.

### -param center

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The point about which the scale is performed.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f">Matrix3x2F</a></b>

The new scale transformation.

## -remarks

This method creates a scale transformation for the specified <i>centerPoint</i> and the 
	 x-axis and y-axis scale factors. If you prefer to create a  
	 <a href="/windows/desktop/Direct2D/d2d1-size-f">D2D1_SIZE_F</a> structure to store the scale factors, call the other <a href="/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f)">Scale</a> method. 

The following illustration shows the size of the square increased 
	 to 130% in both dimensions.
	 The center point of the scaling is the upper-left corner of the square.

<img alt="Illustration of a square scaled by 130% in the x-direction and y-direction" src="images/scale_ovw.png"/>

 For an example, see <a href="/windows/desktop/Direct2D/how-to-scale">How to Scale an Object</a>.

## -see-also

<a href="/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f">Matrix3x2F</a>
