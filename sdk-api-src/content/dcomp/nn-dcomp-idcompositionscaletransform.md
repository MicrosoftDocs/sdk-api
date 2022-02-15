---
UID: NN:dcomp.IDCompositionScaleTransform
title: IDCompositionScaleTransform (dcomp.h)
description: Represents a 2D transformation that affects the scale of a visual along the x-axis and y-axis. The coordinate system is scaled from the specified center point.
helpviewer_keywords: ["IDCompositionScaleTransform","IDCompositionScaleTransform interface [DirectComposition]","IDCompositionScaleTransform interface [DirectComposition]","described","dcomp/IDCompositionScaleTransform","directcomp.idcompositionscaletransform"]
old-location: directcomp\idcompositionscaletransform.htm
tech.root: directcomp
ms.assetid: 8e59c484-b7c5-446a-a5d6-e00371e2c08a
ms.date: 12/05/2018
ms.keywords: IDCompositionScaleTransform, IDCompositionScaleTransform interface [DirectComposition], IDCompositionScaleTransform interface [DirectComposition],described, dcomp/IDCompositionScaleTransform, directcomp.idcompositionscaletransform
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
 - IDCompositionScaleTransform
 - dcomp/IDCompositionScaleTransform
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
 - IDCompositionScaleTransform
---

# IDCompositionScaleTransform interface


## -description

Represents a 2D transformation that affects the scale of a visual along the x-axis and y-axis. The coordinate system is scaled from the specified center point.

## -inheritance

The <b>IDCompositionScaleTransform</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>. <b>IDCompositionScaleTransform</b> also has these types of members:

## -remarks

A scale transform represents the following 3-by-3 matrix:

<img alt="Three-by-three scale matrix" src="./images/scale_transform_3x3matrix.png"/>

The effect is to scale the coordinate system up or down and apply the corresponding translation such that the center point does not move.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
