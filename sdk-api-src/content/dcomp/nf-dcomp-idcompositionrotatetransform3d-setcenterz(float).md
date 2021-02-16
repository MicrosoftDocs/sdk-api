---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetCenterZ(float)
title: IDCompositionRotateTransform3D::SetCenterZ (dcomp.h)
description: Changes the value of the CenterZ property of a 3D rotation transform. The CenterZ property specifies the z-coordinate of the point about which the rotation is performed. The default value is zero.
helpviewer_keywords: ["IDCompositionRotateTransform3D interface [DirectComposition]","SetCenterZ method","IDCompositionRotateTransform3D.SetCenterZ","IDCompositionRotateTransform3D::SetCenterZ","IDCompositionRotateTransform3D::SetCenterZ(float)","SetCenterZ","SetCenterZ method [DirectComposition]","SetCenterZ method [DirectComposition]","IDCompositionRotateTransform3D interface","dcomp/IDCompositionRotateTransform3D::SetCenterZ","directcomp.idcompositionrotatetransform3d_setcenterz_float"]
old-location: directcomp\idcompositionrotatetransform3d_setcenterz_float.htm
tech.root: directcomp
ms.assetid: 56406AD4-F257-444C-8E72-6B9A901D6075
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetCenterZ method, IDCompositionRotateTransform3D.SetCenterZ, IDCompositionRotateTransform3D::SetCenterZ, IDCompositionRotateTransform3D::SetCenterZ(float), SetCenterZ, SetCenterZ method [DirectComposition], SetCenterZ method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetCenterZ, directcomp.idcompositionrotatetransform3d_setcenterz_float
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

# IDCompositionRotateTransform3D::SetCenterZ


## -description

Changes the value of the CenterZ property of a 3D rotation transform. The CenterZ property specifies the z-coordinate of the point about which the rotation is performed. The default value is zero.

## -parameters

### -param centerZ [in]

Type: <b>float</b>

The new z-coordinate of the center point.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>centerZ</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterZ property was previously animated, this method removes the animation and sets the CenterZ property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setcenterx(float)">IDCompositionRotateTransform3D::SetCenterX</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setcentery(float)">IDCompositionRotateTransform3D::SetCenterY</a>