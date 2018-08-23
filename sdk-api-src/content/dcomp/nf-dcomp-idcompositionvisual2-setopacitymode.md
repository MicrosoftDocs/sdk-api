---
UID: NF:dcomp.IDCompositionVisual2.SetOpacityMode
title: IDCompositionVisual2::SetOpacityMode
author: windows-sdk-content
description: Sets the opacity mode for this visual.
old-location: directcomp\idcompositionvisual2_setopacitymode.htm
old-project: directcomp
ms.assetid: 8802266E-9D31-409E-ACE8-62A3E9E93EA3
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionVisual2 interface [DirectComposition],SetOpacityMode method, IDCompositionVisual2.SetOpacityMode, IDCompositionVisual2::SetOpacityMode, SetOpacityMode, SetOpacityMode method [DirectComposition], SetOpacityMode method [DirectComposition],IDCompositionVisual2 interface, dcomp/IDCompositionVisual2::SetOpacityMode, directcomp.idcompositionvisual2_setopacitymode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D2D_VECTOR_4F
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionVisual2.SetOpacityMode
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# IDCompositionVisual2::SetOpacityMode


## -description


Sets the opacity mode for this visual.


## -parameters




### -param mode






#### - opacityMode [in]

	The opacity mode to use when composing the visual to the screen.


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



The opacity mode affects how the Opacity property of an effect group object affects the composition of a visual sub-tree. DirectComposition supports two opacity modes: Layer and Multiply. In Layer mode, each visual sub-tree can be logically viewed as a bitmap that contains the opaque rasterization of that entire sub-tree, to which the opacity value is then applied. In this manner, overlapping opaque surfaces blend with the sub-tree’s background, but not with each other. In contrast, in Multiply mode the opacity is applied individually to each surface as it is composed, so surfaces blend with each other. Multiply mode is faster than Layer mode and always preferred if the visual tree contains entirely non-overlapping contents. However, Multiply mode may produce undesired visual results for overlapping elements.



By default, a visual inherits the opacity mode of its parent visual, which may inherit the opacity mode of its parent visual, and so on. A visual uses the DCOMPOSITION_OPACITY_MODE_LAYER mode if this method is never called for the visual, or if this method is called with DCOMPOSITION_OPACITY_MODE_INHERIT. If no visuals set the opacity mode, the default for the entire visual tree is DCOMPOSITION_OPACITY_MODE_LAYER. 



If the <i>opacityMode</i> parameter is anything other than DCOMPOSITION_OPACITY_MODE_INHERIT, this visual's surfaces are composed with the specified opacity mode. In addition, this opacity mode becomes the new default for the children of the current visual. That is, if the opacity mode of this visual's children is unchanged or explicitly set to DCOMPOSITION_OPACITY_MODE_INHERIT, the surfaces the child visuals are composed using the opacity mode of this visual.





## -see-also




<a href="https://msdn.microsoft.com/785DE91D-718B-4704-88E4-B8FB12586E5F">IDCompositionEffectGroup::SetOpacity</a>



<a href="https://msdn.microsoft.com/D4D04A43-BF00-482A-9CDD-A476BD1CB953">IDCompositionVisual2</a>
 

 

