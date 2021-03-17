---
UID: NF:dcomp.IDCompositionScaleTransform3D.SetScaleX(IDCompositionAnimation)
title: IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation) (dcomp.h)
description: Animates the value of the ScaleX property of a scale transform.
helpviewer_keywords: ["IDCompositionScaleTransform3D interface [DirectComposition]","SetScaleX method","IDCompositionScaleTransform3D.SetScaleX","IDCompositionScaleTransform3D.SetScaleX(IDCompositionAnimation)","IDCompositionScaleTransform3D::SetScaleX","IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation)","IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation*)","SetScaleX","SetScaleX method [DirectComposition]","SetScaleX method [DirectComposition]","IDCompositionScaleTransform3D interface","dcomp/IDCompositionScaleTransform3D::SetScaleX","directcomp.idcompositionscaletransform3d_setscalex_idcompositionanimation"]
old-location: directcomp\idcompositionscaletransform3d_setscalex_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: DAA3F425-344D-4EAE-853A-D4AE2375ADDB
ms.date: 12/05/2018
ms.keywords: IDCompositionScaleTransform3D interface [DirectComposition],SetScaleX method, IDCompositionScaleTransform3D.SetScaleX, IDCompositionScaleTransform3D.SetScaleX(IDCompositionAnimation), IDCompositionScaleTransform3D::SetScaleX, IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation), IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation*), SetScaleX, SetScaleX method [DirectComposition], SetScaleX method [DirectComposition],IDCompositionScaleTransform3D interface, dcomp/IDCompositionScaleTransform3D::SetScaleX, directcomp.idcompositionscaletransform3d_setscalex_idcompositionanimation
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
 - IDCompositionScaleTransform3D::SetScaleX
 - dcomp/IDCompositionScaleTransform3D::SetScaleX
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
 - IDCompositionScaleTransform3D.SetScaleX
---

# IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation)


## -description

Animates the value of the ScaleX property of a scale transform. The ScaleX property specifies the scale factor along the x-axis.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the ScaleX property changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the ScaleX property unless this method is called again. If the ScaleX property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform">IDCompositionScaleTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform3d-setscaley(float)">IDCompositionScaleTransform3D::SetScaleY</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform3d-setscalez(float)">IDCompositionScaleTransform3D::SetScaleZ</a>