---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetAxisY(float)
title: IDCompositionRotateTransform3D::SetAxisY (dcomp.h)
description: Changes the value of the AxisY property of a 3D rotation transform. The AxisY property specifies the y-coordinate for the axis vector of rotation. The default value is zero.
helpviewer_keywords: ["IDCompositionRotateTransform3D interface [DirectComposition]","SetAxisY method","IDCompositionRotateTransform3D.SetAxisY","IDCompositionRotateTransform3D::SetAxisY","IDCompositionRotateTransform3D::SetAxisY(float)","SetAxisY","SetAxisY method [DirectComposition]","SetAxisY method [DirectComposition]","IDCompositionRotateTransform3D interface","dcomp/IDCompositionRotateTransform3D::SetAxisY","directcomp.idcompositionrotatetransform3d_setaxisy_float"]
old-location: directcomp\idcompositionrotatetransform3d_setaxisy_float.htm
tech.root: directcomp
ms.assetid: EEDED20E-B1AC-4464-ABB5-C413E10B3E7E
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetAxisY method, IDCompositionRotateTransform3D.SetAxisY, IDCompositionRotateTransform3D::SetAxisY, IDCompositionRotateTransform3D::SetAxisY(float), SetAxisY, SetAxisY method [DirectComposition], SetAxisY method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetAxisY, directcomp.idcompositionrotatetransform3d_setaxisy_float
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
 - IDCompositionRotateTransform3D::SetAxisY
 - dcomp/IDCompositionRotateTransform3D::SetAxisY
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
 - IDCompositionRotateTransform3D.SetAxisY
---

# IDCompositionRotateTransform3D::SetAxisY


## -description

Changes the value of the AxisY property of a 3D rotation transform. The AxisY property specifies the y-coordinate for the axis vector of rotation.  The default value is zero.

## -parameters

### -param axisY [in]

Type: <b>float</b>

The new y-coordinate for the axis vector of rotation.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

When setting the axis to a non-default value, you should always set all three axis properties (AxisX, AxisY, and AxisZ).

This method fails if the <i>axisY</i> parameter is NaN, positive infinity, or negative infinity.



If the AxisY property was previously animated, this method removes the animation and sets the AxisY property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisx(float)">IDCompositionRotateTransform3D::SetAxisX</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisz(float)">IDCompositionRotateTransform3D::SetAxisZ</a>