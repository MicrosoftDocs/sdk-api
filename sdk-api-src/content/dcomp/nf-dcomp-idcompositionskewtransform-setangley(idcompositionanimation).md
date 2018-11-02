---
UID: NF:dcomp.IDCompositionSkewTransform.SetAngleY(IDCompositionAnimation)
title: IDCompositionSkewTransform::SetAngleY(IDCompositionAnimation)
author: windows-sdk-content
description: Animates the value of the AngleY property of a 2D skew transform.
old-location: directcomp\idcompositionskewtransform_setangley_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: f79ab50f-37f5-43d5-b7df-0cd1b65bdfcd
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDCompositionSkewTransform interface [DirectComposition],SetAngleY method, IDCompositionSkewTransform.SetAngleY, IDCompositionSkewTransform.SetAngleY(IDCompositionAnimation), IDCompositionSkewTransform::SetAngleY, IDCompositionSkewTransform::SetAngleY(IDCompositionAnimation), IDCompositionSkewTransform::SetAngleY(IDCompositionAnimation*), SetAngleY, SetAngleY method [DirectComposition], SetAngleY method [DirectComposition],IDCompositionSkewTransform interface, dcomp/IDCompositionSkewTransform::SetAngleY, directcomp.idcompositionskewtransform_setangley_idcompositionanimation
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
 - IDCompositionSkewTransform.SetAngleY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionSkewTransform::SetAngleY(IDCompositionAnimation)


## -description


Animates the value of the AngleY property of a 2D skew transform. The AngleY property specifies the skew angle along the y-axis.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation object that represents how the value of the AngleY property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the AngleY property unless this method is called again. If the AngleY property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/c1dbc11f-b8e3-487e-84f0-517ebaf65de8">IDCompositionSkewTransform</a>



<a href="https://msdn.microsoft.com/DA4AEE0D-A913-434E-9150-DD6763132041">IDCompositionSkewTransform::SetAngleX</a>
 

 

