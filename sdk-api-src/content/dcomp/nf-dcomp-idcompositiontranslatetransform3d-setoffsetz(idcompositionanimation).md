---
UID: NF:dcomp.IDCompositionTranslateTransform3D.SetOffsetZ(IDCompositionAnimation)
title: IDCompositionTranslateTransform3D::SetOffsetZ(IDCompositionAnimation)
author: windows-sdk-content
description: Animates the value of the OffsetZ property of a 3D translation transform effect. The OffsetZ property specifies the distance to translate along the z-axis.
old-location: directcomp\idcompositiontranslatetransform3d_setoffsetz_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: CAD58523-FBAD-4451-916A-E157F17F0A81
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDCompositionTranslateTransform3D interface [DirectComposition],SetOffsetZ method, IDCompositionTranslateTransform3D.SetOffsetZ, IDCompositionTranslateTransform3D.SetOffsetZ(IDCompositionAnimation), IDCompositionTranslateTransform3D::SetOffsetZ, IDCompositionTranslateTransform3D::SetOffsetZ(IDCompositionAnimation), IDCompositionTranslateTransform3D::SetOffsetZ(IDCompositionAnimation*), SetOffsetZ, SetOffsetZ method [DirectComposition], SetOffsetZ method [DirectComposition],IDCompositionTranslateTransform3D interface, dcomp/IDCompositionTranslateTransform3D::SetOffsetZ, directcomp.idcompositiontranslatetransform3d_setoffsetz_idcompositionanimation
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
 - IDCompositionTranslateTransform3D.SetOffsetZ
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
- IDCompositionTranslateTransform3D.SetOffsetZ
: 
---

# IDCompositionTranslateTransform3D::SetOffsetZ(IDCompositionAnimation)


## -description


Animates the value of the OffsetZ property of a 3D translation transform effect. The OffsetZ property specifies the distance to translate along the z-axis.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the OffsetZ property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the OffsetZ property unless this method is called again. If the OffsetZ property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface that created the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/C265E5FC-F7A1-4E87-8311-C4D0613DD7BC">IDCompositionTranslateTransform3D</a>



<a href="https://msdn.microsoft.com/61EDA0AA-0274-446E-9169-974AB84802FA">IDCompositionTranslateTransform3D::SetOffsetX</a>



<a href="https://msdn.microsoft.com/254DCA74-DB51-442D-9483-F7597643C538">IDCompositionTranslateTransform3D::SetOffsetY</a>
 

 

