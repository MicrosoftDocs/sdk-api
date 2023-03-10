---
UID: NF:dcomp.IDCompositionScaleTransform.SetScaleY(IDCompositionAnimation)
title: IDCompositionScaleTransform::SetScaleY(IDCompositionAnimation) (dcomp.h)
description: Animates the value of the ScaleY property of a 2D scale transform.
helpviewer_keywords: ["IDCompositionScaleTransform interface [DirectComposition]","SetScaleY method","IDCompositionScaleTransform.SetScaleY","IDCompositionScaleTransform.SetScaleY(IDCompositionAnimation)","IDCompositionScaleTransform::SetScaleY","IDCompositionScaleTransform::SetScaleY(IDCompositionAnimation)","IDCompositionScaleTransform::SetScaleY(IDCompositionAnimation*)","SetScaleY","SetScaleY method [DirectComposition]","SetScaleY method [DirectComposition]","IDCompositionScaleTransform interface","dcomp/IDCompositionScaleTransform::SetScaleY","directcomp.idcompositionscaletransform_setscaley_idcompositionanimation"]
old-location: directcomp\idcompositionscaletransform_setscaley_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: B9F747BF-C2FA-442D-B4B7-F76B9559B87E
ms.date: 12/05/2018
ms.keywords: IDCompositionScaleTransform interface [DirectComposition],SetScaleY method, IDCompositionScaleTransform.SetScaleY, IDCompositionScaleTransform.SetScaleY(IDCompositionAnimation), IDCompositionScaleTransform::SetScaleY, IDCompositionScaleTransform::SetScaleY(IDCompositionAnimation), IDCompositionScaleTransform::SetScaleY(IDCompositionAnimation*), SetScaleY, SetScaleY method [DirectComposition], SetScaleY method [DirectComposition],IDCompositionScaleTransform interface, dcomp/IDCompositionScaleTransform::SetScaleY, directcomp.idcompositionscaletransform_setscaley_idcompositionanimation
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
 - IDCompositionScaleTransform::SetScaleY
 - dcomp/IDCompositionScaleTransform::SetScaleY
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
 - IDCompositionScaleTransform.SetScaleY
---

# IDCompositionScaleTransform::SetScaleY(IDCompositionAnimation)


## -description

Animates the value of the ScaleY property of a 2D scale transform. The ScaleY property specifies the scale factor along the y-axis.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the ScaleY property changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the ScaleY property unless this method is called again. If the ScaleY property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform">IDCompositionScaleTransform</a>



<a href="/previous-versions/windows/desktop/legacy/hh449048(v=vs.85)">IDCompositionScaleTransform::SetScaleX</a>