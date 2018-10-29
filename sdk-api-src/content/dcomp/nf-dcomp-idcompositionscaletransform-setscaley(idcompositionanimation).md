---
UID: NF:dcomp.IDCompositionScaleTransform.SetScaleY(IDCompositionAnimation)
title: IDCompositionScaleTransform::SetScaleY(IDCompositionAnimation)
author: windows-sdk-content
description: Animates the value of the ScaleY property of a 2D scale transform.
old-location: directcomp\idcompositionscaletransform_setscaley_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: B9F747BF-C2FA-442D-B4B7-F76B9559B87E
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDCompositionScaleTransform interface [DirectComposition],SetScaleY method, IDCompositionScaleTransform.SetScaleY, IDCompositionScaleTransform.SetScaleY(IDCompositionAnimation), IDCompositionScaleTransform::SetScaleY, IDCompositionScaleTransform::SetScaleY(IDCompositionAnimation), IDCompositionScaleTransform::SetScaleY(IDCompositionAnimation*), SetScaleY, SetScaleY method [DirectComposition], SetScaleY method [DirectComposition],IDCompositionScaleTransform interface, dcomp/IDCompositionScaleTransform::SetScaleY, directcomp.idcompositionscaletransform_setscaley_idcompositionanimation
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
 - IDCompositionScaleTransform.SetScaleY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionScaleTransform::SetScaleY(IDCompositionAnimation)


## -description


Animates the value of the ScaleY property of a 2D scale transform. The ScaleY property specifies the scale factor along the y-axis.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the ScaleY property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the ScaleY property unless this method is called again. If the ScaleY property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform</a>



<a href="https://msdn.microsoft.com/114C4907-280C-4060-9157-30E0E8989251">IDCompositionScaleTransform::SetScaleX</a>
 

 

