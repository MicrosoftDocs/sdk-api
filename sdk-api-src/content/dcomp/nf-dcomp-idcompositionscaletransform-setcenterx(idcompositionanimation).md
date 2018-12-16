---
UID: NF:dcomp.IDCompositionScaleTransform.SetCenterX(IDCompositionAnimation)
title: IDCompositionScaleTransform::SetCenterX(IDCompositionAnimation)
author: windows-sdk-content
description: Animates the value of the CenterX property of a 2D scale transform.
old-location: directcomp\idcompositionscaletransform_setcenterx_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: EA62C748-A741-49A4-8799-0825811D302F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionScaleTransform interface [DirectComposition],SetCenterX method, IDCompositionScaleTransform.SetCenterX, IDCompositionScaleTransform.SetCenterX(IDCompositionAnimation), IDCompositionScaleTransform::SetCenterX, IDCompositionScaleTransform::SetCenterX(IDCompositionAnimation), IDCompositionScaleTransform::SetCenterX(IDCompositionAnimation*), SetCenterX, SetCenterX method [DirectComposition], SetCenterX method [DirectComposition],IDCompositionScaleTransform interface, dcomp/IDCompositionScaleTransform::SetCenterX, directcomp.idcompositionscaletransform_setcenterx_idcompositionanimation
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
 - IDCompositionScaleTransform.SetCenterX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionScaleTransform::SetCenterX(IDCompositionAnimation)


## -description


Animates the value of the CenterX property of a 2D scale transform. The CenterX property specifies the x-coordinate of the point about which scaling is performed.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the CenterX property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the CenterX property unless this method is called again. If the CenterX property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/en-us/library/Hh437392(v=VS.85).aspx">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh448990(v=VS.85).aspx">IDCompositionScaleTransform</a>



<a href="https://msdn.microsoft.com/18A755E6-C6E8-437C-BBB5-58F36F754BE7">IDCompositionScaleTransform::SetCenterY</a>
 

 

