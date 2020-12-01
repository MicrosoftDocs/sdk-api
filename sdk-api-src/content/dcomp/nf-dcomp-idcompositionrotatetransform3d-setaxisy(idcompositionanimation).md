---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetAxisY(IDCompositionAnimation)
title: IDCompositionRotateTransform3D::SetAxisY(IDCompositionAnimation) (dcomp.h)
description: Animates the value of the AxisY property of a 3D rotation transform. The AxisY property specifies the y-coordinate for the axis vector of rotation. The default value is zero.
helpviewer_keywords: ["IDCompositionRotateTransform3D interface [DirectComposition]","SetAxisY method","IDCompositionRotateTransform3D.SetAxisY","IDCompositionRotateTransform3D.SetAxisY(IDCompositionAnimation)","IDCompositionRotateTransform3D::SetAxisY","IDCompositionRotateTransform3D::SetAxisY(IDCompositionAnimation)","IDCompositionRotateTransform3D::SetAxisY(IDCompositionAnimation*)","SetAxisY","SetAxisY method [DirectComposition]","SetAxisY method [DirectComposition]","IDCompositionRotateTransform3D interface","dcomp/IDCompositionRotateTransform3D::SetAxisY","directcomp.idcompositionrotatetransform3d_setaxisy_idcompositionanimation"]
old-location: directcomp\idcompositionrotatetransform3d_setaxisy_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: E4FEC079-D1D6-4279-8AE1-7987312A6DC5
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetAxisY method, IDCompositionRotateTransform3D.SetAxisY, IDCompositionRotateTransform3D.SetAxisY(IDCompositionAnimation), IDCompositionRotateTransform3D::SetAxisY, IDCompositionRotateTransform3D::SetAxisY(IDCompositionAnimation), IDCompositionRotateTransform3D::SetAxisY(IDCompositionAnimation*), SetAxisY, SetAxisY method [DirectComposition], SetAxisY method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetAxisY, directcomp.idcompositionrotatetransform3d_setaxisy_idcompositionanimation
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

# IDCompositionRotateTransform3D::SetAxisY(IDCompositionAnimation)


## -description

Animates the value of the AxisY property of a 3D rotation transform. The AxisY property specifies the y-coordinate for the axis vector of rotation. The default value is zero.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the AxisY property changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

When setting the axis to a non-default value, you should always set all three axis properties (AxisX, AxisY, and AxisZ).

This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the AxisY property unless this method is called again. If the AxisY property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected 3D transform. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisx(float)">IDCompositionRotateTransform3D::SetAxisX</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisz(float)">IDCompositionRotateTransform3D::SetAxisZ</a>