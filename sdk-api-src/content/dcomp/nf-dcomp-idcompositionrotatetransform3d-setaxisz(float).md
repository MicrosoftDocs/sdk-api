---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetAxisZ(float)
title: IDCompositionRotateTransform3D::SetAxisZ (dcomp.h)
description: Changes the value of the AxisZ property of a 3D rotation transform. The AxisZ property specifies the z-coordinate for the axis vector of rotation. The default value is 1.0.
helpviewer_keywords: ["IDCompositionRotateTransform3D interface [DirectComposition]","SetAxisZ method","IDCompositionRotateTransform3D.SetAxisZ","IDCompositionRotateTransform3D::SetAxisZ","IDCompositionRotateTransform3D::SetAxisZ(float)","SetAxisZ","SetAxisZ method [DirectComposition]","SetAxisZ method [DirectComposition]","IDCompositionRotateTransform3D interface","dcomp/IDCompositionRotateTransform3D::SetAxisZ","directcomp.idcompositionrotatetransform3d_setaxisz_float"]
old-location: directcomp\idcompositionrotatetransform3d_setaxisz_float.htm
tech.root: directcomp
ms.assetid: 2150E564-0E19-40E9-9D33-53EA17917A8F
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetAxisZ method, IDCompositionRotateTransform3D.SetAxisZ, IDCompositionRotateTransform3D::SetAxisZ, IDCompositionRotateTransform3D::SetAxisZ(float), SetAxisZ, SetAxisZ method [DirectComposition], SetAxisZ method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetAxisZ, directcomp.idcompositionrotatetransform3d_setaxisz_float
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
 - IDCompositionRotateTransform3D::SetAxisZ
 - dcomp/IDCompositionRotateTransform3D::SetAxisZ
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
 - IDCompositionRotateTransform3D.SetAxisZ
---

# IDCompositionRotateTransform3D::SetAxisZ


## -description

Changes the value of the AxisZ property of a 3D rotation transform. The AxisZ property specifies the z-coordinate for the axis vector of rotation. The default value is 1.0.

## -parameters

### -param axisZ [in]

Type: <b>float</b>

The new z-coordinate for the axis vector of rotation.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

When setting the axis to a non-default value, you should always set all three axis properties (AxisX, AxisY, and AxisZ).

This method fails if the <i>axisZ</i> parameter is NaN, positive infinity, or negative infinity.



If the AxisZ property was previously animated, this method removes the animation and sets the AxisX property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisx(float)">IDCompositionRotateTransform3D::SetAxisX</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisy(float)">IDCompositionRotateTransform3D::SetAxisY</a>