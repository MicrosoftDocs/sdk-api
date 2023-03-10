---
UID: NN:dcomp.IDCompositionSkewTransform
title: IDCompositionSkewTransform (dcomp.h)
description: Represents a 2D transformation that affects the skew of a visual along the x-axis and y-axis. The coordinate system is skewed around the specified center point.
helpviewer_keywords: ["IDCompositionSkewTransform","IDCompositionSkewTransform interface [DirectComposition]","IDCompositionSkewTransform interface [DirectComposition]","described","dcomp/IDCompositionSkewTransform","directcomp.idcompositionskewtransform"]
old-location: directcomp\idcompositionskewtransform.htm
tech.root: directcomp
ms.assetid: c1dbc11f-b8e3-487e-84f0-517ebaf65de8
ms.date: 12/05/2018
ms.keywords: IDCompositionSkewTransform, IDCompositionSkewTransform interface [DirectComposition], IDCompositionSkewTransform interface [DirectComposition],described, dcomp/IDCompositionSkewTransform, directcomp.idcompositionskewtransform
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
 - IDCompositionSkewTransform
 - dcomp/IDCompositionSkewTransform
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
 - IDCompositionSkewTransform
---

# IDCompositionSkewTransform interface


## -description

Represents a 2D transformation that affects the skew of a visual along the x-axis and y-axis. The coordinate system is skewed around the specified center point.

## -inheritance

The <b>IDCompositionSkewTransform</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>. <b>IDCompositionSkewTransform</b> also has these types of members:

## -remarks

A skew transform represents the following 3-by-3 matrix: 

<img alt="Three-by-three skew matrix" src="./images/skew_transform_3x3matrix.png"/>

The effect is to slant the coordinate system along the x-axis and y-axis such that a rectangle becomes a parallelogram, and to apply the corresponding translation such that the center point does not move.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
