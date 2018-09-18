---
UID: NF:dcomp.IDCompositionScaleTransform3D.SetCenterX(IDCompositionAnimation)
title: IDCompositionScaleTransform3D::SetCenterX(IDCompositionAnimation)
author: windows-sdk-content
description: Animates the value of the CenterX property of a 3D scale transform.
old-location: directcomp\idcompositionscaletransform3d_setcenterx_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 36F9ACCF-2F70-4F9F-A2E5-8DAF27325B1D
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDCompositionScaleTransform3D interface [DirectComposition],SetCenterX method, IDCompositionScaleTransform3D.SetCenterX, IDCompositionScaleTransform3D.SetCenterX(IDCompositionAnimation), IDCompositionScaleTransform3D::SetCenterX, IDCompositionScaleTransform3D::SetCenterX(IDCompositionAnimation), IDCompositionScaleTransform3D::SetCenterX(IDCompositionAnimation*), SetCenterX, SetCenterX method [DirectComposition], SetCenterX method [DirectComposition],IDCompositionScaleTransform3D interface, dcomp/IDCompositionScaleTransform3D::SetCenterX, directcomp.idcompositionscaletransform3d_setcenterx_idcompositionanimation
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
 - IDCompositionScaleTransform3D.SetCenterX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionScaleTransform3D::SetCenterX(IDCompositionAnimation)


## -description


Animates the value of the CenterX property of a 3D scale transform. The CenterX property specifies the x-coordinate of the point about which scaling is performed.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the CenterX property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the CenterX property unless this method is called again. If the CenterX property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform3D</a>



<a href="https://msdn.microsoft.com/C650032E-3344-4BE8-9018-F57EFECEBF61">IDCompositionScaleTransform3D::SetCenterY</a>



<a href="https://msdn.microsoft.com/1A5C63FE-2378-4274-8ADD-04A88B60FF8F">IDCompositionScaleTransform3D::SetCenterZ</a>
 

 

