---
UID: NF:dcomp.IDCompositionVisual.SetEffect
title: IDCompositionVisual::SetEffect (dcomp.h)
description: Sets the Effect property of this visual.
helpviewer_keywords: ["IDCompositionVisual interface [DirectComposition]","SetEffect method","IDCompositionVisual.SetEffect","IDCompositionVisual::SetEffect","SetEffect","SetEffect method [DirectComposition]","SetEffect method [DirectComposition]","IDCompositionVisual interface","dcomp/IDCompositionVisual::SetEffect","directcomp.idcompositionvisual_seteffect"]
old-location: directcomp\idcompositionvisual_seteffect.htm
tech.root: directcomp
ms.assetid: CCA785F6-869C-460A-AF54-573BDE798685
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetEffect method, IDCompositionVisual.SetEffect, IDCompositionVisual::SetEffect, SetEffect, SetEffect method [DirectComposition], SetEffect method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetEffect, directcomp.idcompositionvisual_seteffect
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
 - IDCompositionVisual::SetEffect
 - dcomp/IDCompositionVisual::SetEffect
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
 - IDCompositionVisual.SetEffect
---

# IDCompositionVisual::SetEffect


## -description

Sets the Effect property of this visual. The Effect property modifies how the subtree that is rooted at this visual is blended with the background, and can apply a 3D perspective transform to the visual.

## -parameters

### -param effect [in, optional]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffect">IDCompositionEffect</a>*</b>

A pointer to an effect object. This parameter can be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method creates an implicit off-screen surface to which the subtree that is rooted at this visual is composed. The surface is used as one of the inputs to the specified effect. The output of the effect is composed directly to the composition target. Some effects also use the composition target as another implicit input. This is typically the case for compositional or blend effects such as opacity, where the composition target is considered to be the "background." In that case, any visuals that are "behind" the current visual are included in the composition target when the current visual is rendered and are considered to be the "background" that this visual composes to.



If this visual is not the root of a visual tree and one of its ancestors also has an effect applied to it, the off-screen surface created by the closest ancestor is the composition target to which this visual's effect is composed. Otherwise, the composition target is the root composition target. As a consequence, the background for compositional and blend effects includes only the visuals up to the closest ancestor that itself has an effect. Conversely, any effects applied to visuals under the current visual use the newly created off-screen surface as the background, which may affect how those visuals ultimately compose on top of what the end user perceives as being "behind" those visuals.



If the <i>effect</i> parameter is NULL,  no bitmap effect is applied to this visual. Any previous effects that were associated with this visual are removed. The off-screen surface is also removed and the visual subtree is composed directly to the parent composition target, which may also affect how compositional or blend effects under this visual are rendered.



This method fails if <i>effect</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface that created this visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffect">IDCompositionEffect</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffectgroup">IDCompositionEffectGroup</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform3d">IDCompositionMatrixTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform3d">IDCompositionScaleTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d">IDCompositionTranslateTransform3D</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>