---
UID: NN:dcomp.IDCompositionRotateTransform3D
title: IDCompositionRotateTransform3D (dcomp.h)
description: Represents a 3D transformation that affects the rotation of a visual along an arbitrary axis in 3D space. The coordinate system is rotated around the specified center point.
helpviewer_keywords: ["IDCompositionRotateTransform3D","IDCompositionRotateTransform3D interface [DirectComposition]","IDCompositionRotateTransform3D interface [DirectComposition]","described","dcomp/IDCompositionRotateTransform3D","directcomp.idcompositionrotatetransform3d"]
old-location: directcomp\idcompositionrotatetransform3d.htm
tech.root: directcomp
ms.assetid: BEC58B57-66A1-4645-A0B8-D546334E1E23
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D, IDCompositionRotateTransform3D interface [DirectComposition], IDCompositionRotateTransform3D interface [DirectComposition],described, dcomp/IDCompositionRotateTransform3D, directcomp.idcompositionrotatetransform3d
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionRotateTransform3D
 - dcomp/IDCompositionRotateTransform3D
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionRotateTransform3D
---

# IDCompositionRotateTransform3D interface


## -description

Represents a 3D transformation that affects the rotation of a visual along an arbitrary axis in 3D space. The coordinate system is rotated around the specified center point.

## -inheritance

The <b>IDCompositionRotateTransform3D</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>. <b>IDCompositionRotateTransform3D</b> also has these types of members:

## -remarks

A 3D rotate transform represents the following 4-by-4 matrix:

<img alt="Four-by-four 3D rotate transformation matrix" src="./images/3D_rotate_transform_4x4matrix.png"/>

where the <i>offsetX</i>, <i>offsetY</i>, and <i>offsetZ</i> values of the matrix are the following: 

<img alt="Values of the four-by-four 3D rotate transformation matrix" src="./images/3D_rotate_transform_matrix_values.png"/>

The effect is to rotate the coordinate system clockwise or counter-clockwise around the specified axis, and to apply the corresponding translation such that the center point does not move.

A new 3D rotation transform object has a default static value of zero for the Angle, CenterX, CenterY, AxisX, and AxisY properties, and a default static value of 1.0 for the AxisZ property.

When setting the axis to a non-default value, you should always set all three axis properties (AxisX, AxisY, and AxisZ).

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">IDCompositionEffectGroup::SetTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>
