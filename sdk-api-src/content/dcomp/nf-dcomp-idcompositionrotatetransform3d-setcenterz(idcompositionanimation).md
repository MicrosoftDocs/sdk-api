---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetCenterZ(IDCompositionAnimation)
title: IDCompositionRotateTransform3D::SetCenterZ(IDCompositionAnimation) (dcomp.h)
description: Animates the value of the CenterZ property of a 3D rotation transform. The CenterZ property specifies the z-coordinate of the point about which the rotation is performed. The default value is zero.
helpviewer_keywords: ["IDCompositionRotateTransform3D interface [DirectComposition]","SetCenterZ method","IDCompositionRotateTransform3D.SetCenterZ","IDCompositionRotateTransform3D.SetCenterZ(IDCompositionAnimation)","IDCompositionRotateTransform3D::SetCenterZ","IDCompositionRotateTransform3D::SetCenterZ(IDCompositionAnimation)","IDCompositionRotateTransform3D::SetCenterZ(IDCompositionAnimation*)","SetCenterZ","SetCenterZ method [DirectComposition]","SetCenterZ method [DirectComposition]","IDCompositionRotateTransform3D interface","dcomp/IDCompositionRotateTransform3D::SetCenterZ","directcomp.idcompositionrotatetransform3d_setcenterz_idcompositionanimation"]
old-location: directcomp\idcompositionrotatetransform3d_setcenterz_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: D78841F5-17A1-4B52-9928-7EEB878DFBF9
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetCenterZ method, IDCompositionRotateTransform3D.SetCenterZ, IDCompositionRotateTransform3D.SetCenterZ(IDCompositionAnimation), IDCompositionRotateTransform3D::SetCenterZ, IDCompositionRotateTransform3D::SetCenterZ(IDCompositionAnimation), IDCompositionRotateTransform3D::SetCenterZ(IDCompositionAnimation*), SetCenterZ, SetCenterZ method [DirectComposition], SetCenterZ method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetCenterZ, directcomp.idcompositionrotatetransform3d_setcenterz_idcompositionanimation
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
 - IDCompositionRotateTransform3D::SetCenterZ
 - dcomp/IDCompositionRotateTransform3D::SetCenterZ
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
 - IDCompositionRotateTransform3D.SetCenterZ
---

# IDCompositionRotateTransform3D::SetCenterZ(IDCompositionAnimation)


## -description

Animates the value of the CenterZ property of a 3D rotation transform.  The CenterZ property specifies the z-coordinate of the point about which the rotation is performed. The default value is zero.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the CenterZ property changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the CenterZ property unless this method is called again. If the CenterZ property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setcenterx(float)">IDCompositionRotateTransform3D::SetCenterX</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setcentery(float)">IDCompositionRotateTransform3D::SetCenterY</a>