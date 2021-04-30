---
UID: NF:dcomp.IDCompositionSkewTransform.SetAngleY(IDCompositionAnimation)
title: IDCompositionSkewTransform::SetAngleY(IDCompositionAnimation) (dcomp.h)
description: Animates the value of the AngleY property of a 2D skew transform.
helpviewer_keywords: ["IDCompositionSkewTransform interface [DirectComposition]","SetAngleY method","IDCompositionSkewTransform.SetAngleY","IDCompositionSkewTransform.SetAngleY(IDCompositionAnimation)","IDCompositionSkewTransform::SetAngleY","IDCompositionSkewTransform::SetAngleY(IDCompositionAnimation)","IDCompositionSkewTransform::SetAngleY(IDCompositionAnimation*)","SetAngleY","SetAngleY method [DirectComposition]","SetAngleY method [DirectComposition]","IDCompositionSkewTransform interface","dcomp/IDCompositionSkewTransform::SetAngleY","directcomp.idcompositionskewtransform_setangley_idcompositionanimation"]
old-location: directcomp\idcompositionskewtransform_setangley_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: f79ab50f-37f5-43d5-b7df-0cd1b65bdfcd
ms.date: 12/05/2018
ms.keywords: IDCompositionSkewTransform interface [DirectComposition],SetAngleY method, IDCompositionSkewTransform.SetAngleY, IDCompositionSkewTransform.SetAngleY(IDCompositionAnimation), IDCompositionSkewTransform::SetAngleY, IDCompositionSkewTransform::SetAngleY(IDCompositionAnimation), IDCompositionSkewTransform::SetAngleY(IDCompositionAnimation*), SetAngleY, SetAngleY method [DirectComposition], SetAngleY method [DirectComposition],IDCompositionSkewTransform interface, dcomp/IDCompositionSkewTransform::SetAngleY, directcomp.idcompositionskewtransform_setangley_idcompositionanimation
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
 - IDCompositionSkewTransform::SetAngleY
 - dcomp/IDCompositionSkewTransform::SetAngleY
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
 - IDCompositionSkewTransform.SetAngleY
---

# IDCompositionSkewTransform::SetAngleY(IDCompositionAnimation)


## -description

Animates the value of the AngleY property of a 2D skew transform. The AngleY property specifies the skew angle along the y-axis.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that represents how the value of the AngleY property changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the AngleY property unless this method is called again. If the AngleY property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionskewtransform">IDCompositionSkewTransform</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionskewtransform-setanglex(float)">IDCompositionSkewTransform::SetAngleX</a>