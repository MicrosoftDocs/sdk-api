---
UID: NF:uianimation.IUIAnimationVariable2.SetVariableCurveChangeHandler
title: IUIAnimationVariable2::SetVariableCurveChangeHandler
author: windows-sdk-content
description: Specifies a handler for changes to the animation curve of the animation variable.
old-location: uianimation\iuianimationvariable2_setvariablecurvechangehandler.htm
old-project: UIAnimation
ms.assetid: 98C95C85-30C9-4E3E-82FE-E3D4C7ECAE0B
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIAnimationVariable2 interface [Windows Animation],SetVariableCurveChangeHandler method, IUIAnimationVariable2.SetVariableCurveChangeHandler, IUIAnimationVariable2::SetVariableCurveChangeHandler, SetVariableCurveChangeHandler, SetVariableCurveChangeHandler method [Windows Animation], SetVariableCurveChangeHandler method [Windows Animation],IUIAnimationVariable2 interface, uianimation.iuianimationvariable2_setvariablecurvechangehandler, uianimation/IUIAnimationVariable2::SetVariableCurveChangeHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAnimation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationVariable2.SetVariableCurveChangeHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable2::SetVariableCurveChangeHandler


## -description


Specifies a handler for changes to the animation curve of the animation variable. 


## -parameters




### -param handler [in, optional]

A pointer to the handler for changes to the animation curve of the animation variable. This parameter can be <b>NULL</b>.




## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">IUIAnimationVariable2</a>



<a href="https://msdn.microsoft.com/C3F992CE-6C12-40AF-BA22-10C82E597314">IUIAnimationVariableCurveChangeHandler2</a>
 

 

