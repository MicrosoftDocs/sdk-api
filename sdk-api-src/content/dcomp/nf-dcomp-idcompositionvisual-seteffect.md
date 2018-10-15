---
UID: NF:dcomp.IDCompositionVisual.SetEffect
title: IDCompositionVisual::SetEffect
author: windows-sdk-content
description: Sets the Effect property of this visual.
old-location: directcomp\idcompositionvisual_seteffect.htm
tech.root: directcomp
ms.assetid: CCA785F6-869C-460A-AF54-573BDE798685
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetEffect method, IDCompositionVisual.SetEffect, IDCompositionVisual::SetEffect, SetEffect, SetEffect method [DirectComposition], SetEffect method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetEffect, directcomp.idcompositionvisual_seteffect
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
 - IDCompositionVisual.SetEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual::SetEffect


## -description


Sets the Effect property of this visual. The Effect property modifies how the subtree that is rooted at this visual is blended with the background, and can apply a 3D perspective transform to the visual. 


## -parameters




### -param effect [in, optional]

Type: <b><a href="https://msdn.microsoft.com/9C9DFECD-0EC0-446C-8CCC-BB7979B01575">IDCompositionEffect</a>*</b>

A pointer to an effect object. This parameter can be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method creates an implicit off-screen surface to which the subtree that is rooted at this visual is composed. The surface is used as one of the inputs to the specified effect. The output of the effect is composed directly to the composition target. Some effects also use the composition target as another implicit input. This is typically the case for compositional or blend effects such as opacity, where the composition target is considered to be the "background." In that case, any visuals that are "behind" the current visual are included in the composition target when the current visual is rendered and are considered to be the "background" that this visual composes to.



If this visual is not the root of a visual tree and one of its ancestors also has an effect applied to it, the off-screen surface created by the closest ancestor is the composition target to which this visual's effect is composed. Otherwise, the composition target is the root composition target. As a consequence, the background for compositional and blend effects includes only the visuals up to the closest ancestor that itself has an effect. Conversely, any effects applied to visuals under the current visual use the newly created off-screen surface as the background, which may affect how those visuals ultimately compose on top of what the end user perceives as being "behind" those visuals.



If the <i>effect</i> parameter is NULL,  no bitmap effect is applied to this visual. Any previous effects that were associated with this visual are removed. The off-screen surface is also removed and the visual subtree is composed directly to the parent composition target, which may also affect how compositional or blend effects under this visual are rendered.



This method fails if <i>effect</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface that created this visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.






## -see-also




<a href="https://msdn.microsoft.com/9C9DFECD-0EC0-446C-8CCC-BB7979B01575">IDCompositionEffect</a>



<a href="https://msdn.microsoft.com/B8C5A4D8-F161-4383-B117-B89E85C65B19">IDCompositionEffectGroup</a>



<a href="https://msdn.microsoft.com/56C9A564-2504-4940-B850-D280C8E0CF82">IDCompositionMatrixTransform3D</a>



<a href="https://msdn.microsoft.com/BEC58B57-66A1-4645-A0B8-D546334E1E23">IDCompositionRotateTransform3D</a>



<a href="https://msdn.microsoft.com/0526B772-EA84-40B2-88D6-CFB1A70A1D5A">IDCompositionScaleTransform3D</a>



<a href="https://msdn.microsoft.com/C265E5FC-F7A1-4E87-8311-C4D0613DD7BC">IDCompositionTranslateTransform3D</a>



<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>
 

 

