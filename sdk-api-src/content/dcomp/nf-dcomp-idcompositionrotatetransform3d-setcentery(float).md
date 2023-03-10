---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetCenterY(float)
title: IDCompositionRotateTransform3D::SetCenterY (dcomp.h)
description: Changes the value of the CenterY property of a 3D rotation transform. The CenterY property specifies the y-coordinate of the point about which the rotation is performed. The default value is zero.
helpviewer_keywords: ["IDCompositionRotateTransform3D interface [DirectComposition]","SetCenterY method","IDCompositionRotateTransform3D.SetCenterY","IDCompositionRotateTransform3D::SetCenterY","IDCompositionRotateTransform3D::SetCenterY(float)","SetCenterY","SetCenterY method [DirectComposition]","SetCenterY method [DirectComposition]","IDCompositionRotateTransform3D interface","dcomp/IDCompositionRotateTransform3D::SetCenterY","directcomp.idcompositionrotatetransform3d_setcentery_float"]
old-location: directcomp\idcompositionrotatetransform3d_setcentery_float.htm
tech.root: directcomp
ms.assetid: 3A7E562C-52ED-45A4-B473-6ACBF6A9C0E9
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetCenterY method, IDCompositionRotateTransform3D.SetCenterY, IDCompositionRotateTransform3D::SetCenterY, IDCompositionRotateTransform3D::SetCenterY(float), SetCenterY, SetCenterY method [DirectComposition], SetCenterY method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetCenterY, directcomp.idcompositionrotatetransform3d_setcentery_float
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
 - IDCompositionRotateTransform3D::SetCenterY
 - dcomp/IDCompositionRotateTransform3D::SetCenterY
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
 - IDCompositionRotateTransform3D.SetCenterY
---

# IDCompositionRotateTransform3D::SetCenterY


## -description

Changes the value of the CenterY property of a 3D rotation transform. The CenterY property specifies the y-coordinate of the point about which the rotation is performed. The default value is zero.

## -parameters

### -param centerY [in]

Type: <b>float</b>

The new y-coordinate of the center point.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>centerY</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterY property was previously animated, this method removes the animation and sets the CenterY property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>



<a href="/previous-versions/windows/desktop/legacy/hh448982(v=vs.85)">IDCompositionRotateTransform3D::SetCenterX</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setcenterz(float)">IDCompositionRotateTransform3D::SetCenterZ</a>