---
UID: NF:dcomp.IDCompositionScaleTransform3D.SetScaleX(IDCompositionAnimation)
title: IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation) (dcomp.h)
author: windows-sdk-content
description: Animates the value of the ScaleX property of a scale transform.
old-location: directcomp\idcompositionscaletransform3d_setscalex_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: DAA3F425-344D-4EAE-853A-D4AE2375ADDB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionScaleTransform3D interface [DirectComposition],SetScaleX method, IDCompositionScaleTransform3D.SetScaleX, IDCompositionScaleTransform3D.SetScaleX(IDCompositionAnimation), IDCompositionScaleTransform3D::SetScaleX, IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation), IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation*), SetScaleX, SetScaleX method [DirectComposition], SetScaleX method [DirectComposition],IDCompositionScaleTransform3D interface, dcomp/IDCompositionScaleTransform3D::SetScaleX, directcomp.idcompositionscaletransform3d_setscalex_idcompositionanimation
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
 - IDCompositionScaleTransform3D.SetScaleX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionScaleTransform3D::SetScaleX(IDCompositionAnimation)


## -description


Animates the value of the ScaleX property of a scale transform. The ScaleX property specifies the scale factor along the x-axis.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the ScaleX property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the ScaleX property unless this method is called again. If the ScaleX property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform3D</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449024(v=VS.85).aspx">IDCompositionScaleTransform3D::SetScaleY</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449030(v=VS.85).aspx">IDCompositionScaleTransform3D::SetScaleZ</a>
 

 

