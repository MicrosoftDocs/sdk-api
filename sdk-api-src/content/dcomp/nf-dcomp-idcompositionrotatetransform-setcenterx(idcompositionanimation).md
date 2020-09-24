---
UID: NF:dcomp.IDCompositionRotateTransform.SetCenterX(IDCompositionAnimation)
title: IDCompositionRotateTransform::SetCenterX(IDCompositionAnimation) (dcomp.h)
description: Animates the value of the CenterX property of a 2D rotation transform.
helpviewer_keywords: ["IDCompositionRotateTransform interface [DirectComposition]","SetCenterX method","IDCompositionRotateTransform.SetCenterX","IDCompositionRotateTransform.SetCenterX(IDCompositionAnimation)","IDCompositionRotateTransform::SetCenterX","IDCompositionRotateTransform::SetCenterX(IDCompositionAnimation)","IDCompositionRotateTransform::SetCenterX(IDCompositionAnimation*)","SetCenterX","SetCenterX method [DirectComposition]","SetCenterX method [DirectComposition]","IDCompositionRotateTransform interface","dcomp/IDCompositionRotateTransform::SetCenterX","directcomp.idcompositionrotatetransform_setcenterx_idcompositionanimation"]
old-location: directcomp\idcompositionrotatetransform_setcenterx_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 9E04CEF1-FC36-46AE-BD63-3154BDB26034
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform interface [DirectComposition],SetCenterX method, IDCompositionRotateTransform.SetCenterX, IDCompositionRotateTransform.SetCenterX(IDCompositionAnimation), IDCompositionRotateTransform::SetCenterX, IDCompositionRotateTransform::SetCenterX(IDCompositionAnimation), IDCompositionRotateTransform::SetCenterX(IDCompositionAnimation*), SetCenterX, SetCenterX method [DirectComposition], SetCenterX method [DirectComposition],IDCompositionRotateTransform interface, dcomp/IDCompositionRotateTransform::SetCenterX, directcomp.idcompositionrotatetransform_setcenterx_idcompositionanimation
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
 - IDCompositionRotateTransform::SetCenterX
 - dcomp/IDCompositionRotateTransform::SetCenterX
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
 - IDCompositionRotateTransform.SetCenterX
---

# IDCompositionRotateTransform::SetCenterX(IDCompositionAnimation)


## -description

Animates the value of the CenterX property of a 2D rotation transform.  The CenterX property specifies the x-coordinate of the point about which the rotation is performed.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the CenterX property changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the CenterX property unless this method is called again. If the CenterX property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform">IDCompositionRotateTransform</a>



<a href="/previous-versions/windows/desktop/legacy/hh448988(v=vs.85)">IDCompositionRotateTransform::SetCenterY</a>