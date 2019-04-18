---
UID: NF:dcomp.IDCompositionVisual.SetTransformParent
title: IDCompositionVisual::SetTransformParent (dcomp.h)
author: windows-sdk-content
description: Sets the TransformParent property of this visual. The TransformParent property establishes the coordinate system relative to which this visual is composed.
old-location: directcomp\idcompositionvisual_settransformparent.htm
tech.root: directcomp
ms.assetid: 06C02E3D-27FF-4E11-87C2-7D8281A69601
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetTransformParent method, IDCompositionVisual.SetTransformParent, IDCompositionVisual::SetTransformParent, SetTransformParent, SetTransformParent method [DirectComposition], SetTransformParent method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetTransformParent, directcomp.idcompositionvisual_settransformparent
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
 - IDCompositionVisual.SetTransformParent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionVisual::SetTransformParent


## -description


Sets the TransformParent property of this visual. The TransformParent property establishes the coordinate system relative to which this visual is composed.


## -parameters




### -param visual [in, optional]

Type: <b><a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>*</b>

The new visual that establishes the base coordinate system for this visual. This parameter can be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



The coordinate system of a visual is modified by the OffsetX, OffsetY, and Transform properties. Normally, these properties define the coordinate system of a visual relative to its immediate parent. This method specifies the  visual relative to which the coordinate system for this visual is based. The specified visual must be an ancestor of the current visual. If it is not an ancestor, the coordinate system is based on this visual's immediate parent, just as if the TransformParent property were set to NULL. Because visuals can be reparented, this property can take effect again if the specified visual becomes an ancestor of the target visual through a reparenting operation.



If the <i>visual</i> parameter is NULL, the coordinate system is always transformed relative to the visual's immediate parent. This is the default behavior if this method is not used. 



This method fails if the <i>visual</i> parameter is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface as this visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>
 

 

