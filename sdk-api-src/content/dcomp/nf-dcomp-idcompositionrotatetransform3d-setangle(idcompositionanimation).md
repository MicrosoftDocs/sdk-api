---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetAngle(IDCompositionAnimation)
title: IDCompositionRotateTransform3D::SetAngle(IDCompositionAnimation) (dcomp.h)
author: windows-sdk-content
description: Animates the value of the Angle property of a 3D rotation transform. The Angle property specifies the rotation angle. The default value is zero.
old-location: directcomp\idcompositionrotatetransform3d_setangle_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 71EBFC30-E148-416D-8BE3-9E65955388A1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetAngle method, IDCompositionRotateTransform3D.SetAngle, IDCompositionRotateTransform3D.SetAngle(IDCompositionAnimation), IDCompositionRotateTransform3D::SetAngle, IDCompositionRotateTransform3D::SetAngle(IDCompositionAnimation), IDCompositionRotateTransform3D::SetAngle(IDCompositionAnimation*), SetAngle, SetAngle method [DirectComposition], SetAngle method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetAngle, directcomp.idcompositionrotatetransform3d_setangle_idcompositionanimation
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionRotateTransform3D.SetAngle"
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
 - IDCompositionRotateTransform3D.SetAngle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionRotateTransform3D::SetAngle(IDCompositionAnimation)


## -description


Animates the value of the Angle property of a 3D rotation transform. The Angle property specifies the rotation angle. The default value is zero.


## -parameters




### -param animation [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the Angle property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the Angle property unless this method is called again. If the Angle property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected 3D transform. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>
 

 

