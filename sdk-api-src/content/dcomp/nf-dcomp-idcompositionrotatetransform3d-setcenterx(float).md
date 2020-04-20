---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetCenterX(float)
title: IDCompositionRotateTransform3D::SetCenterX (dcomp.h)
description: Changes the value of the CenterX property of a 3D rotation transform. The CenterX property specifies the x-coordinate of the point about which the rotation is performed. The default value is zero.helpviewer_keywords: ["IDCompositionRotateTransform3D interface [DirectComposition]","SetCenterX method","IDCompositionRotateTransform3D.SetCenterX","IDCompositionRotateTransform3D::SetCenterX","IDCompositionRotateTransform3D::SetCenterX(float)","SetCenterX","SetCenterX method [DirectComposition]","SetCenterX method [DirectComposition]","IDCompositionRotateTransform3D interface","dcomp/IDCompositionRotateTransform3D::SetCenterX","directcomp.idcompositionrotatetransform3d_setcenterx_float"]
old-location: directcomp\idcompositionrotatetransform3d_setcenterx_float.htm
tech.root: directcomp
ms.assetid: 669A3002-23C0-44FA-ABC9-B4AE1C8A2C81
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetCenterX method, IDCompositionRotateTransform3D.SetCenterX, IDCompositionRotateTransform3D::SetCenterX, IDCompositionRotateTransform3D::SetCenterX(float), SetCenterX, SetCenterX method [DirectComposition], SetCenterX method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetCenterX, directcomp.idcompositionrotatetransform3d_setcenterx_float
f1_keywords:
- dcomp/IDCompositionRotateTransform3D.SetCenterX
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
- IDCompositionRotateTransform3D.SetCenterX
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionRotateTransform3D::SetCenterX


## -description


Changes the value of the CenterX property of a 3D rotation transform. The CenterX property specifies the x-coordinate of the point about which the rotation is performed. The default value is zero.


## -parameters




### -param centerX [in]

Type: <b>float</b>

The new x-coordinate of the center point.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>centerX</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterX property was previously animated, this method removes the animation and sets the CenterX property to the specified static value.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>



<a href="https://docs.microsoft.com/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setcentery(float)">IDCompositionRotateTransform3D::SetCenterY</a>



<a href="https://docs.microsoft.com/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setcenterz(float)">IDCompositionRotateTransform3D::SetCenterZ</a>
 

 

