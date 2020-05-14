---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetAxisX(float)
title: IDCompositionRotateTransform3D::SetAxisX (dcomp.h)
description: Changes the value of the AxisX property of a 3D rotation transform. The AxisX property specifies the x-coordinate for the axis vector of rotation. The default value is zero.
helpviewer_keywords: ["IDCompositionRotateTransform3D interface [DirectComposition]","SetAxisX method","IDCompositionRotateTransform3D.SetAxisX","IDCompositionRotateTransform3D::SetAxisX","IDCompositionRotateTransform3D::SetAxisX(float)","SetAxisX","SetAxisX method [DirectComposition]","SetAxisX method [DirectComposition]","IDCompositionRotateTransform3D interface","dcomp/IDCompositionRotateTransform3D::SetAxisX","directcomp.idcompositionrotatetransform3d_setaxisx_float"]
old-location: directcomp\idcompositionrotatetransform3d_setaxisx_float.htm
tech.root: directcomp
ms.assetid: C31C84EC-40D1-4DB0-AA7E-70E611F6AF62
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetAxisX method, IDCompositionRotateTransform3D.SetAxisX, IDCompositionRotateTransform3D::SetAxisX, IDCompositionRotateTransform3D::SetAxisX(float), SetAxisX, SetAxisX method [DirectComposition], SetAxisX method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetAxisX, directcomp.idcompositionrotatetransform3d_setaxisx_float
f1_keywords:
- dcomp/IDCompositionRotateTransform3D.SetAxisX
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dcomp.dll
api_name:
- IDCompositionRotateTransform3D.SetAxisX
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionRotateTransform3D::SetAxisX


## -description


Changes the value of the AxisX property of a 3D rotation transform. The AxisX property specifies the x-coordinate for the axis vector of rotation. The default value is zero.


## -parameters




### -param axisX [in]

Type: <b>float</b>

The new x-coordinate for the axis vector of rotation. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



When setting the axis to a non-default value, you should always set all three axis properties (AxisX, AxisY, and AxisZ).

This method fails if the <i>axisX</i> parameter is NaN, positive infinity, or negative infinity.



If the AxisX property was previously animated, this method removes the animation and sets the AxisX property to the specified static value.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisy(float)">IDCompositionRotateTransform3D::SetAxisY</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisz(float)">IDCompositionRotateTransform3D::SetAxisZ</a>
 

 

