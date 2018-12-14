---
UID: NF:dcomp.IDCompositionScaleTransform3D.SetCenterY(IDCompositionAnimation)
title: IDCompositionScaleTransform3D::SetCenterY(IDCompositionAnimation)
author: windows-sdk-content
description: Animates the value of the CenterY property of a 3D scale transform.
old-location: directcomp\idcompositionscaletransform3d_setcentery_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 3FF6E893-1764-4182-A6D9-3B71915CEA39
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionScaleTransform3D interface [DirectComposition],SetCenterY method, IDCompositionScaleTransform3D.SetCenterY, IDCompositionScaleTransform3D.SetCenterY(IDCompositionAnimation), IDCompositionScaleTransform3D::SetCenterY, IDCompositionScaleTransform3D::SetCenterY(IDCompositionAnimation), IDCompositionScaleTransform3D::SetCenterY(IDCompositionAnimation*), SetCenterY, SetCenterY method [DirectComposition], SetCenterY method [DirectComposition],IDCompositionScaleTransform3D interface, dcomp/IDCompositionScaleTransform3D::SetCenterY, directcomp.idcompositionscaletransform3d_setcentery_idcompositionanimation
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
 - IDCompositionScaleTransform3D.SetCenterY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionScaleTransform3D::SetCenterY(IDCompositionAnimation)


## -description


Animates the value of the CenterY property of a 3D scale transform. The CenterY property specifies the y-coordinate of the point about which scaling is performed.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the CenterY property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the CenterY property unless this method is called again. If the CenterY property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/en-us/library/Hh437392(v=VS.85).aspx">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh448990(v=VS.85).aspx">IDCompositionScaleTransform3D</a>



<a href="https://msdn.microsoft.com/959F8530-D2D5-46BC-9F29-F1DFC8029C12">IDCompositionScaleTransform3D::SetCenterX</a>



<a href="https://msdn.microsoft.com/1A5C63FE-2378-4274-8ADD-04A88B60FF8F">IDCompositionScaleTransform3D::SetCenterZ</a>
 

 

