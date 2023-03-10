---
UID: NN:dcomp.IDCompositionRotateTransform
title: IDCompositionRotateTransform (dcomp.h)
description: Represents a 2D transformation that affects the rotation of a visual around the z-axis. The coordinate system is rotated around the specified center point.
helpviewer_keywords: ["IDCompositionRotateTransform","IDCompositionRotateTransform interface [DirectComposition]","IDCompositionRotateTransform interface [DirectComposition]","described","dcomp/IDCompositionRotateTransform","directcomp.idcompositionrotatetransform"]
old-location: directcomp\idcompositionrotatetransform.htm
tech.root: directcomp
ms.assetid: 6c92bd6b-4479-45c2-986c-0a6c91248361
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform, IDCompositionRotateTransform interface [DirectComposition], IDCompositionRotateTransform interface [DirectComposition],described, dcomp/IDCompositionRotateTransform, directcomp.idcompositionrotatetransform
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
 - IDCompositionRotateTransform
 - dcomp/IDCompositionRotateTransform
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
 - IDCompositionRotateTransform
---

# IDCompositionRotateTransform interface


## -description

Represents a 2D transformation that affects the rotation of a visual around the z-axis. The coordinate system is rotated around the specified center point.

## -inheritance

The <b>IDCompositionRotateTransform</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>. <b>IDCompositionRotateTransform</b> also has these types of members:

## -remarks

A rotate transform represents the following 3-by-3 matrix:

<img alt="Three-by-three transformation matrix" src="./images/rotate_transform_3x3matrix.png"/>

The effect is to rotate the coordinate system clockwise or counter-clockwise, and to apply the corresponding translation such that the center point does not move.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
