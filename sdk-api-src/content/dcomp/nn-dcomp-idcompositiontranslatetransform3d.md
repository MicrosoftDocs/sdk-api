---
UID: NN:dcomp.IDCompositionTranslateTransform3D
title: IDCompositionTranslateTransform3D (dcomp.h)
description: Represents a 3D transformation that affects the offset of a visual along the x-axis, y-axis, and z-axis.
helpviewer_keywords: ["IDCompositionTranslateTransform3D","IDCompositionTranslateTransform3D interface [DirectComposition]","IDCompositionTranslateTransform3D interface [DirectComposition]","described","dcomp/IDCompositionTranslateTransform3D","directcomp.idcompositiontranslatetransform3d"]
old-location: directcomp\idcompositiontranslatetransform3d.htm
tech.root: directcomp
ms.assetid: C265E5FC-F7A1-4E87-8311-C4D0613DD7BC
ms.date: 12/05/2018
ms.keywords: IDCompositionTranslateTransform3D, IDCompositionTranslateTransform3D interface [DirectComposition], IDCompositionTranslateTransform3D interface [DirectComposition],described, dcomp/IDCompositionTranslateTransform3D, directcomp.idcompositiontranslatetransform3d
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
 - IDCompositionTranslateTransform3D
 - dcomp/IDCompositionTranslateTransform3D
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
 - IDCompositionTranslateTransform3D
---

# IDCompositionTranslateTransform3D interface


## -description

Represents a 3D transformation that affects the offset of a visual along the x-axis, y-axis, and z-axis.

## -inheritance

The <b>IDCompositionTranslateTransform3D</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>. <b>IDCompositionTranslateTransform3D</b> also has these types of members:

## -remarks

A 3D translation transform represents the following 4-by-4 matrix:
      

<img alt="Four-by-four translation matrix" src="./images/3D_translate_transform_4x4matrix.png"/>

The effect is to offset the blending position of the visual's subtree by <i>x</i>, <i>y</i>, and <i>z</i>.

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">IDCompositionEffectGroup::SetTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>
