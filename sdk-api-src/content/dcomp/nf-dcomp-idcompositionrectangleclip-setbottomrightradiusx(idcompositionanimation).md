---
UID: NF:dcomp.IDCompositionRectangleClip.SetBottomRightRadiusX(IDCompositionAnimation)
title: IDCompositionRectangleClip::SetBottomRightRadiusX(IDCompositionAnimation)
author: windows-sdk-content
description: Animates the value of the BottomRightRadiusX property of this clip. The BottomRightRadiusX property specifies the x radius of the ellipse that rounds the lower-right corner of the clip.
old-location: directcomp\idcompositionrectangleclip_setbottomrightradiusx_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 52233FC5-B3C9-45F8-B522-ED403B404AD9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionRectangleClip interface [DirectComposition],SetBottomRightRadiusX method, IDCompositionRectangleClip.SetBottomRightRadiusX, IDCompositionRectangleClip.SetBottomRightRadiusX(IDCompositionAnimation), IDCompositionRectangleClip::SetBottomRightRadiusX, IDCompositionRectangleClip::SetBottomRightRadiusX(IDCompositionAnimation), IDCompositionRectangleClip::SetBottomRightRadiusX(IDCompositionAnimation*), SetBottomRightRadiusX, SetBottomRightRadiusX method [DirectComposition], SetBottomRightRadiusX method [DirectComposition],IDCompositionRectangleClip interface, dcomp/IDCompositionRectangleClip::SetBottomRightRadiusX, directcomp.idcompositionrectangleclip_setbottomrightradiusx_idcompositionanimation
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
 - IDCompositionRectangleClip.SetBottomRightRadiusX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionRectangleClip::SetBottomRightRadiusX(IDCompositionAnimation)


## -description


Animates the value of the BottomRightRadiusX property of this clip. The BottomRightRadiusX property  specifies the x radius of the ellipse that rounds the lower-right corner of the clip.


## -parameters




### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the x radius changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the x radius unless this method is called again. If the x radius was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://msdn.microsoft.com/486bcdb9-e353-4ca2-b24c-af863dda7470">IDCompositionRectangleClip</a>
 

 

