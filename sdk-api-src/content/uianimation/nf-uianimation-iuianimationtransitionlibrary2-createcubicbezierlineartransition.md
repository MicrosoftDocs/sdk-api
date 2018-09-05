---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateCubicBezierLinearTransition
title: IUIAnimationTransitionLibrary2::CreateCubicBezierLinearTransition
author: windows-sdk-content
description: Creates a cubic Bézier linear scalar transition.
old-location: uianimation\iuianimationtransitionlibrary2_createcubicbezierlineartransition.htm
old-project: UIAnimation
ms.assetid: 1943D3B6-0DA6-4F1B-B52D-F121BAC6BE68
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateCubicBezierLinearTransition, CreateCubicBezierLinearTransition method [Windows Animation], CreateCubicBezierLinearTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateCubicBezierLinearTransition method, IUIAnimationTransitionLibrary2.CreateCubicBezierLinearTransition, IUIAnimationTransitionLibrary2::CreateCubicBezierLinearTransition, uianimation.iuianimationtransitionlibrary2_createcubicbezierlineartransition, uianimation/IUIAnimationTransitionLibrary2::CreateCubicBezierLinearTransition
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
 - IUIAnimationTransitionLibrary2.CreateCubicBezierLinearTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary2::CreateCubicBezierLinearTransition


## -description


Creates a cubic Bézier linear scalar transition.


## -parameters




### -param duration [in]

The duration of the transition.


### -param finalValue [in]

The value of the animation variable at the end of the transition.


### -param x1 [in]

The x-coordinate of the first control point.


### -param y1 [in]

The y-coordinate of the first control point.


### -param x2 [in]

The x-coordinate of the second control point.


### -param y2 [in]

The y-coordinate of the second control point.


### -param ppTransition [out]

The new cubic Bézier linear transition.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



During a cubic Bézier linear transition, the value of the animation variable changes from its initial value to the <i>finalValue</i> over the <i>duration</i> of the transition. The ordered pairs, (x1, y1) and (x2, y2), act as control points that provide directional information to transform the linear path of the transition into a smooth parametric curve.

The following figure shows the change in value over time for an animation variable during a cubic Bézier linear transition.

<img alt="Diagram showing a cubic Bezier linear transition" src="Images/cubicbezierlineartransition.png"/>



## -see-also




<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">IUIAnimationTransitionLibrary2</a>
 

 

