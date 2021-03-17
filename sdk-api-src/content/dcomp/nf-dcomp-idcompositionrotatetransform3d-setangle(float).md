---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetAngle(float)
title: IDCompositionRotateTransform3D::SetAngle(float) (dcomp.h)
description: Changes the value of the Angle property of a 3D rotation transform. The Angle property specifies the rotation angle. The default value is zero.
helpviewer_keywords: ["IDCompositionRotateTransform3D interface [DirectComposition]","SetAngle method","IDCompositionRotateTransform3D.SetAngle","IDCompositionRotateTransform3D.SetAngle(float)","IDCompositionRotateTransform3D::SetAngle","IDCompositionRotateTransform3D::SetAngle(float)","SetAngle","SetAngle method [DirectComposition]","SetAngle method [DirectComposition]","IDCompositionRotateTransform3D interface","dcomp/IDCompositionRotateTransform3D::SetAngle","directcomp.idcompositionrotatetransform3d_setangle_float"]
old-location: directcomp\idcompositionrotatetransform3d_setangle_float.htm
tech.root: directcomp
ms.assetid: A1C367E1-530C-4D4F-B93E-8C53C3DCF373
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetAngle method, IDCompositionRotateTransform3D.SetAngle, IDCompositionRotateTransform3D.SetAngle(float), IDCompositionRotateTransform3D::SetAngle, IDCompositionRotateTransform3D::SetAngle(float), SetAngle, SetAngle method [DirectComposition], SetAngle method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetAngle, directcomp.idcompositionrotatetransform3d_setangle_float
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
 - IDCompositionRotateTransform3D::SetAngle
 - dcomp/IDCompositionRotateTransform3D::SetAngle
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
 - IDCompositionRotateTransform3D.SetAngle
---

# IDCompositionRotateTransform3D::SetAngle(float)


## -description

Changes the value of the Angle property of a 3D rotation transform. The Angle property specifies the rotation angle. The default value is zero.

## -parameters

### -param angle [in]

Type: <b>float</b>

The new rotation angle, in degrees. Positive values are interpreted as the thumb-down (into the page), right hand rule where the thumb points in the Z direction and the fingers follow a clockwise direction.  Negative values are interpreted as the thumb-up (out of the page), right hand rule. For values less than -360 or greater than 360, the values wrap around and are treated as if the mathematical operation mod(360) was applied.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>angle</i> parameter is NaN, positive infinity, or negative infinity.



If the Angle property was previously animated, this method removes the animation and sets the Angle property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>