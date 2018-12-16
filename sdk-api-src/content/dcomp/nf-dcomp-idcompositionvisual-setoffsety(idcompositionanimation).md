---
UID: NF:dcomp.IDCompositionVisual.SetOffsetY(IDCompositionAnimation)
title: IDCompositionVisual::SetOffsetY(IDCompositionAnimation)
author: windows-sdk-content
description: Animates the value of the OffsetY property of this visual.
old-location: directcomp\idcompositionvisual_setoffsety_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 48B42D13-B41A-484E-B65E-BB4D56A963DA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetOffsetY method, IDCompositionVisual.SetOffsetY, IDCompositionVisual.SetOffsetY(IDCompositionAnimation), IDCompositionVisual::SetOffsetY, IDCompositionVisual::SetOffsetY(IDCompositionAnimation), IDCompositionVisual::SetOffsetY(IDCompositionAnimation*), SetOffsetY, SetOffsetY method [DirectComposition], SetOffsetY method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetOffsetY, directcomp.idcompositionvisual_setoffsety_idcompositionanimation
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
 - IDCompositionVisual.SetOffsetY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual::SetOffsetY(IDCompositionAnimation)


## -description


Animates the value of the OffsetY property of this visual.  The OffsetY property specifies the new offset of the visual along the y-axis, relative to the parent visual.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the OffsetY property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the animation object referenced by the <i>animation</i> parameter is changed after this call, the change does not affect the OffsetY property unless this method is called again. If the OffsetY property was previously animated, this method replaces that animation with the new animation.

This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/en-us/library/Hh437392(v=VS.85).aspx">IDCompositionDevice</a> interface that created this visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh449139(v=VS.85).aspx">IDCompositionVisual</a>



<a href="https://msdn.microsoft.com/0EFCDE12-3BF1-4D1F-8E28-54F3D7EEFFC1">IDCompositionVisual::SetOffsetX</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

