---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetAxisZ(IDCompositionAnimation)
title: IDCompositionRotateTransform3D::SetAxisZ(IDCompositionAnimation) (dcomp.h)
description: Animates the value of the AxisZ property of a 3D rotation transform. The AxisZ property specifies the z-coordinate for the axis vector of rotation. The default value is 1.0.
helpviewer_keywords: ["IDCompositionRotateTransform3D interface [DirectComposition]","SetAxisZ method","IDCompositionRotateTransform3D.SetAxisZ","IDCompositionRotateTransform3D.SetAxisZ(IDCompositionAnimation)","IDCompositionRotateTransform3D::SetAxisZ","IDCompositionRotateTransform3D::SetAxisZ(IDCompositionAnimation)","IDCompositionRotateTransform3D::SetAxisZ(IDCompositionAnimation*)","SetAxisZ","SetAxisZ method [DirectComposition]","SetAxisZ method [DirectComposition]","IDCompositionRotateTransform3D interface","dcomp/IDCompositionRotateTransform3D::SetAxisZ","directcomp.idcompositionrotatetransform3d_setaxisz_idcompositionanimation"]
old-location: directcomp\idcompositionrotatetransform3d_setaxisz_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 2264BB6F-D2B7-49A8-959A-FA5AA935F6CC
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetAxisZ method, IDCompositionRotateTransform3D.SetAxisZ, IDCompositionRotateTransform3D.SetAxisZ(IDCompositionAnimation), IDCompositionRotateTransform3D::SetAxisZ, IDCompositionRotateTransform3D::SetAxisZ(IDCompositionAnimation), IDCompositionRotateTransform3D::SetAxisZ(IDCompositionAnimation*), SetAxisZ, SetAxisZ method [DirectComposition], SetAxisZ method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetAxisZ, directcomp.idcompositionrotatetransform3d_setaxisz_idcompositionanimation
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

# IDCompositionRotateTransform3D::SetAxisZ(IDCompositionAnimation)


## -description

Animates the value of the AxisZ property of a 3D rotation transform. The AxisZ property specifies the z-coordinate for the axis vector of rotation. The default value is 1.0.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the AxisZ property changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

When setting the axis to a non-default value, you should always set all three axis properties (AxisX, AxisY, and AxisZ).

This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the AxisZ property unless this method is called again. If the AxisZ property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected 3D transform. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.


The default value is 0.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisx(float)">IDCompositionRotateTransform3D::SetAxisX</a>



<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisy(float)">IDCompositionRotateTransform3D::SetAxisY</a>