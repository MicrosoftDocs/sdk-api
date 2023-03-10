---
UID: NN:dcomp.IDCompositionScaleTransform3D
title: IDCompositionScaleTransform3D (dcomp.h)
description: Represents a 3D transformation effect that affects the scale of a visual along the x-axis, y-axis, and z-axis. The coordinate system is scaled from the specified center point.
helpviewer_keywords: ["IDCompositionScaleTransform3D","IDCompositionScaleTransform3D interface [DirectComposition]","IDCompositionScaleTransform3D interface [DirectComposition]","described","dcomp/IDCompositionScaleTransform3D","directcomp.idcompositionscaletransform3d"]
old-location: directcomp\idcompositionscaletransform3d.htm
tech.root: directcomp
ms.assetid: 0526B772-EA84-40B2-88D6-CFB1A70A1D5A
ms.date: 12/05/2018
ms.keywords: IDCompositionScaleTransform3D, IDCompositionScaleTransform3D interface [DirectComposition], IDCompositionScaleTransform3D interface [DirectComposition],described, dcomp/IDCompositionScaleTransform3D, directcomp.idcompositionscaletransform3d
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
 - IDCompositionScaleTransform3D
 - dcomp/IDCompositionScaleTransform3D
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
 - IDCompositionScaleTransform3D
---

# IDCompositionScaleTransform3D interface


## -description

Represents a 3D transformation effect that affects the scale of a visual along the x-axis, y-axis, and z-axis. The coordinate system is scaled from the specified center point.

## -inheritance

The <b>IDCompositionScaleTransform3D</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>. <b>IDCompositionScaleTransform3D</b> also has these types of members:

## -remarks

A 3D scale transform represents the following 4-by-4 matrix:

<img alt="Four-by-four 3D scale matrix" src="./images/3D_scale_transform_4x4matrix.png"/>

The effect is to scale the blending of the visual's subtree up or down, and apply the corresponding translation such that the center point does not move.

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">IDCompositionEffectGroup::SetTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>
