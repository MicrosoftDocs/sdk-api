---
UID: NF:dcomp.IDCompositionTranslateTransform3D.SetOffsetX(IDCompositionAnimation)
title: IDCompositionTranslateTransform3D::SetOffsetX(IDCompositionAnimation) (dcomp.h)
description: Animates the value of the OffsetX property of a 3D translation transform effect. The OffsetX property specifies the distance to translate along the x-axis.
helpviewer_keywords: ["IDCompositionTranslateTransform3D interface [DirectComposition]","SetOffsetX method","IDCompositionTranslateTransform3D.SetOffsetX","IDCompositionTranslateTransform3D.SetOffsetX(IDCompositionAnimation)","IDCompositionTranslateTransform3D::SetOffsetX","IDCompositionTranslateTransform3D::SetOffsetX(IDCompositionAnimation)","IDCompositionTranslateTransform3D::SetOffsetX(IDCompositionAnimation*)","SetOffsetX","SetOffsetX method [DirectComposition]","SetOffsetX method [DirectComposition]","IDCompositionTranslateTransform3D interface","dcomp/IDCompositionTranslateTransform3D::SetOffsetX","directcomp.idcompositiontranslatetransform3d_setoffsetx_idcompositionanimation"]
old-location: directcomp\idcompositiontranslatetransform3d_setoffsetx_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 0F68BE7E-C413-429F-BA0C-36A26B2DFA72
ms.date: 12/05/2018
ms.keywords: IDCompositionTranslateTransform3D interface [DirectComposition],SetOffsetX method, IDCompositionTranslateTransform3D.SetOffsetX, IDCompositionTranslateTransform3D.SetOffsetX(IDCompositionAnimation), IDCompositionTranslateTransform3D::SetOffsetX, IDCompositionTranslateTransform3D::SetOffsetX(IDCompositionAnimation), IDCompositionTranslateTransform3D::SetOffsetX(IDCompositionAnimation*), SetOffsetX, SetOffsetX method [DirectComposition], SetOffsetX method [DirectComposition],IDCompositionTranslateTransform3D interface, dcomp/IDCompositionTranslateTransform3D::SetOffsetX, directcomp.idcompositiontranslatetransform3d_setoffsetx_idcompositionanimation
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
 - IDCompositionTranslateTransform3D::SetOffsetX
 - dcomp/IDCompositionTranslateTransform3D::SetOffsetX
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
 - IDCompositionTranslateTransform3D.SetOffsetX
---

# IDCompositionTranslateTransform3D::SetOffsetX(IDCompositionAnimation)


## -description

Animates the value of the OffsetX property of a 3D translation transform effect. The OffsetX property specifies the distance to translate along the x-axis.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the OffsetX property changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the OffsetX property unless this method is called again. If the OffsetX property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform3d">IDCompositionTranslateTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositiontranslatetransform3d-setoffsety(float)">IDCompositionTranslateTransform3D::SetOffsetY</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositiontranslatetransform3d-setoffsetz(float)">IDCompositionTranslateTransform3D::SetOffsetZ</a>