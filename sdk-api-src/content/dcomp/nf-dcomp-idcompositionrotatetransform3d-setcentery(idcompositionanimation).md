---
UID: NF:dcomp.IDCompositionRotateTransform3D.SetCenterY(IDCompositionAnimation)
title: IDCompositionRotateTransform3D::SetCenterY(IDCompositionAnimation)
author: windows-sdk-content
description: Animates the value of the CenterY property of a 3D rotation transform. The CenterY property specifies the y-coordinate of the point about which the rotation is performed. The default value is zero.
old-location: directcomp\idcompositionrotatetransform3d_setcentery_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 051E01E0-1A1B-4724-A8F2-F12F2EC27C4C
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDCompositionRotateTransform3D interface [DirectComposition],SetCenterY method, IDCompositionRotateTransform3D.SetCenterY, IDCompositionRotateTransform3D.SetCenterY(IDCompositionAnimation), IDCompositionRotateTransform3D::SetCenterY, IDCompositionRotateTransform3D::SetCenterY(IDCompositionAnimation), IDCompositionRotateTransform3D::SetCenterY(IDCompositionAnimation*), SetCenterY, SetCenterY method [DirectComposition], SetCenterY method [DirectComposition],IDCompositionRotateTransform3D interface, dcomp/IDCompositionRotateTransform3D::SetCenterY, directcomp.idcompositionrotatetransform3d_setcentery_idcompositionanimation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDCompositionRotateTransform3D.SetCenterY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dcomp.h
: 
- IDCompositionRotateTransform3D.SetCenterY
: 
---

# IDCompositionRotateTransform3D::SetCenterY(IDCompositionAnimation)


## -description


Animates the value of the CenterY property of a 3D rotation transform.  The CenterY property specifies the y-coordinate of the point about which the rotation is performed. The default value is zero.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the CenterY property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the CenterY property unless this method is called again. If the CenterY property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/BEC58B57-66A1-4645-A0B8-D546334E1E23">IDCompositionRotateTransform3D</a>



<a href="https://msdn.microsoft.com/2E4924A5-64D0-4415-B345-0DE9A0900258">IDCompositionRotateTransform3D::SetCenterX</a>



<a href="https://msdn.microsoft.com/7FF293B6-8FAE-4277-8C07-EBD4E819E2A0">IDCompositionRotateTransform3D::SetCenterZ</a>
 

 

