---
UID: NF:d2d1helper.Matrix3x2F.Skew
title: Matrix3x2F::Skew (d2d1helper.h)
description: Creates a skew transformation that has the specified x-axis and y-axis values and center point.
helpviewer_keywords: ["D2D1.Matrix3x2F.Skew","D2D1::Matrix3x2F::Skew","Matrix3x2F interface [Direct2D]","Skew method","Matrix3x2F.Skew","Matrix3x2F::Skew","Skew","Skew method [Direct2D]","Skew method [Direct2D]","Matrix3x2F interface","d2d1helper/Matrix3x2F::Skew","direct2d.matrix3x2f_skew"]
old-location: direct2d\matrix3x2f_skew.htm
tech.root: Direct2D
ms.assetid: 7d53aaff-3a6f-4949-9835-a30027d247dd
ms.date: 12/05/2018
ms.keywords: D2D1.Matrix3x2F.Skew, D2D1::Matrix3x2F::Skew, Matrix3x2F interface [Direct2D],Skew method, Matrix3x2F.Skew, Matrix3x2F::Skew, Skew, Skew method [Direct2D], Skew method [Direct2D],Matrix3x2F interface, d2d1helper/Matrix3x2F::Skew, direct2d.matrix3x2f_skew
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
 - Matrix3x2F::Skew
 - d2d1helper/Matrix3x2F::Skew
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
 - Matrix3x2F.Skew
---

# Matrix3x2F::Skew


## -description

Creates a skew transformation that has the specified x-axis and y-axis values and center point.

## -parameters

### -param angleX

Type: <b>FLOAT</b>

The x-axis skew angle, which is measured in degrees counterclockwise from the y-axis.

### -param angleY

Type: <b>FLOAT</b>

The y-axis skew angle, which is measured in degrees clockwise from the x-axis.

### -param center

Type: <b><a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The point about which the skew is performed.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f">Matrix3x2F</a></b>

The new skew transformation.

## -remarks

The typical y-axis skew means skews the angle in degrees counterclockwise from the x-axis. However, because the y-axis in Direct2D is inverted, the y-axis skew angle in Direct2D means skew the angle in degrees clockwise from the x-axis.

For example, the following illustration shows the rectangle skewed with y-axis skew angle of 30 degrees.  Notice that the angle is 30 degrees clockwise from the x-axis. 

<img alt="Illustration of a rectangle that is skewed along the y-axis for 30 degrees" src="./images/skewy.png"/>

#### Examples

For an example, see <a href="/windows/desktop/Direct2D/how-to-skew">How to Skew an Object</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f">Matrix3x2F</a>