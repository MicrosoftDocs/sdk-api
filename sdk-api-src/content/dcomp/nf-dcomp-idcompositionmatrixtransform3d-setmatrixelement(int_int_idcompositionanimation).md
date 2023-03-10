---
UID: NF:dcomp.IDCompositionMatrixTransform3D.SetMatrixElement(int,int,IDCompositionAnimation)
title: IDCompositionMatrixTransform3D::SetMatrixElement(int,int,IDCompositionAnimation) (dcomp.h)
description: Animates the value of one element of the matrix of this 3D transform.
helpviewer_keywords: ["IDCompositionMatrixTransform3D interface [DirectComposition]","SetMatrixElement method","IDCompositionMatrixTransform3D.SetMatrixElement","IDCompositionMatrixTransform3D.SetMatrixElement(int","int","IDCompositionAnimation)","IDCompositionMatrixTransform3D::SetMatrixElement","IDCompositionMatrixTransform3D::SetMatrixElement(int","int","IDCompositionAnimation)","IDCompositionMatrixTransform3D::SetMatrixElement(int","int","IDCompositionAnimation*)","SetMatrixElement","SetMatrixElement method [DirectComposition]","SetMatrixElement method [DirectComposition]","IDCompositionMatrixTransform3D interface","dcomp/IDCompositionMatrixTransform3D::SetMatrixElement","directcomp.idcompositionmatrixtransform3d_setmatrixelement_idcompositionanimation"]
old-location: directcomp\idcompositionmatrixtransform3d_setmatrixelement_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 099AB3AB-D0F8-4D25-B407-83C77810F34D
ms.date: 12/05/2018
ms.keywords: IDCompositionMatrixTransform3D interface [DirectComposition],SetMatrixElement method, IDCompositionMatrixTransform3D.SetMatrixElement, IDCompositionMatrixTransform3D.SetMatrixElement(int,int,IDCompositionAnimation), IDCompositionMatrixTransform3D::SetMatrixElement, IDCompositionMatrixTransform3D::SetMatrixElement(int,int,IDCompositionAnimation), IDCompositionMatrixTransform3D::SetMatrixElement(int,int,IDCompositionAnimation*), SetMatrixElement, SetMatrixElement method [DirectComposition], SetMatrixElement method [DirectComposition],IDCompositionMatrixTransform3D interface, dcomp/IDCompositionMatrixTransform3D::SetMatrixElement, directcomp.idcompositionmatrixtransform3d_setmatrixelement_idcompositionanimation
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
 - IDCompositionMatrixTransform3D::SetMatrixElement
 - dcomp/IDCompositionMatrixTransform3D::SetMatrixElement
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
 - IDCompositionMatrixTransform3D.SetMatrixElement
---

# IDCompositionMatrixTransform3D::SetMatrixElement(int,int,IDCompositionAnimation)


## -description

Animates the value of one element of the matrix of this 3D transform.

## -parameters

### -param row [in]

Type: <b>int</b>

The row index of the element to change. This value must be between 0 and 3, inclusive.

### -param column [in]

Type: <b>int</b>

The column index of the element to change. This value must be between 0 and 3, inclusive.

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the value of the specified element changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the specified element unless this method is called again. If the specified element was previously animated, calling this method replaces the previous animation with the new animation.

This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected transform. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform3d">IDCompositionMatrixTransform3D</a>