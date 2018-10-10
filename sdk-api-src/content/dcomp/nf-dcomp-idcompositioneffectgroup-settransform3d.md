---
UID: NF:dcomp.IDCompositionEffectGroup.SetTransform3D
title: IDCompositionEffectGroup::SetTransform3D
author: windows-sdk-content
description: Sets the 3D transformation effect object that modifies the rasterization of the visuals that this effect group is applied to.
old-location: directcomp\idcompositioneffectgroup_settransform3d.htm
tech.root: directcomp
ms.assetid: 40935581-D45C-496B-90B9-152963F0B55A
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IDCompositionEffectGroup interface [DirectComposition],SetTransform3D method, IDCompositionEffectGroup.SetTransform3D, IDCompositionEffectGroup::SetTransform3D, SetTransform3D, SetTransform3D method [DirectComposition], SetTransform3D method [DirectComposition],IDCompositionEffectGroup interface, dcomp/IDCompositionEffectGroup::SetTransform3D, directcomp.idcompositioneffectgroup_settransform3d
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
 - IDCompositionEffectGroup.SetTransform3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionEffectGroup::SetTransform3D


## -description


Sets the 3D transformation effect object that modifies the rasterization of the visuals that this effect group is applied to.


## -parameters




### -param transform3D [in, optional]

Type: <b><a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a> interface or one of its derived interfaces. This parameter can be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if <i>transform3D</i> is an invalid pointer, or if the pointer was not created by the same <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface as this effect group. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.



If the <i>transform3D</i> parameter is NULL, the effect group does not apply any perspective transformations to the visuals. Setting the transform to NULL is equivalent to setting the transform to an <a href="https://msdn.microsoft.com/56C9A564-2504-4940-B850-D280C8E0CF82">IDCompositionMatrixTransform3D</a> object where the specified matrix is the identity matrix. However, an application should use a NULL transform whenever possible because it is slightly faster. 







## -see-also




<a href="https://msdn.microsoft.com/B8C5A4D8-F161-4383-B117-B89E85C65B19">IDCompositionEffectGroup</a>



<a href="https://msdn.microsoft.com/56C9A564-2504-4940-B850-D280C8E0CF82">IDCompositionMatrixTransform3D</a>



<a href="https://msdn.microsoft.com/BEC58B57-66A1-4645-A0B8-D546334E1E23">IDCompositionRotateTransform3D</a>



<a href="https://msdn.microsoft.com/0526B772-EA84-40B2-88D6-CFB1A70A1D5A">IDCompositionScaleTransform3D</a>



<a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a>



<a href="https://msdn.microsoft.com/C265E5FC-F7A1-4E87-8311-C4D0613DD7BC">IDCompositionTranslateTransform3D</a>
 

 

