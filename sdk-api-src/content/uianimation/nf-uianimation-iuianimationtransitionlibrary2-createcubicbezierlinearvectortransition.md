---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateCubicBezierLinearVectorTransition
title: IUIAnimationTransitionLibrary2::CreateCubicBezierLinearVectorTransition (uianimation.h)
description: Creates a cubic Bézier linear vector transition for each specified dimension.
helpviewer_keywords: ["CreateCubicBezierLinearVectorTransition","CreateCubicBezierLinearVectorTransition method [Windows Animation]","CreateCubicBezierLinearVectorTransition method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateCubicBezierLinearVectorTransition method","IUIAnimationTransitionLibrary2.CreateCubicBezierLinearVectorTransition","IUIAnimationTransitionLibrary2::CreateCubicBezierLinearVectorTransition","uianimation.iuianimationtransitionlibrary2_createcubicbezierlinearvectortransition","uianimation/IUIAnimationTransitionLibrary2::CreateCubicBezierLinearVectorTransition"]
old-location: uianimation\iuianimationtransitionlibrary2_createcubicbezierlinearvectortransition.htm
tech.root: UIAnimation
ms.assetid: AA1630D4-7E8B-4B1D-B3F8-1BDB9C3F73C7
ms.date: 12/05/2018
ms.keywords: CreateCubicBezierLinearVectorTransition, CreateCubicBezierLinearVectorTransition method [Windows Animation], CreateCubicBezierLinearVectorTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateCubicBezierLinearVectorTransition method, IUIAnimationTransitionLibrary2.CreateCubicBezierLinearVectorTransition, IUIAnimationTransitionLibrary2::CreateCubicBezierLinearVectorTransition, uianimation.iuianimationtransitionlibrary2_createcubicbezierlinearvectortransition, uianimation/IUIAnimationTransitionLibrary2::CreateCubicBezierLinearVectorTransition
req.header: uianimation.h
req.include-header: 
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
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationTransitionLibrary2::CreateCubicBezierLinearVectorTransition
 - uianimation/IUIAnimationTransitionLibrary2::CreateCubicBezierLinearVectorTransition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationTransitionLibrary2.CreateCubicBezierLinearVectorTransition
---

# IUIAnimationTransitionLibrary2::CreateCubicBezierLinearVectorTransition


## -description

Creates a cubic Bézier linear vector transition for each specified dimension.

## -parameters

### -param duration [in]

The duration of the transition.

### -param finalValue [in]

A vector (of size <i>cDimension</i>) that contains  the final values of the animation variable at the end of the transition.

### -param cDimension [in]

The number of dimensions to apply the transition. This parameter specifies the number of values listed in <i>finalValue</i>.

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

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During a cubic Bézier linear transition, the value of the animation variable changes from its initial value to the <i>finalValue</i> over the <i>duration</i> of the transition. The ordered pairs, (x1, y1) and (x2, y2), act as control points that provide directional information to transform the linear path of the transition into a smooth parametric curve.

The following figure shows the change in value over time of an animation variable during a cubic Bézier linear transition.

<img alt="Diagram showing a cubic Bezier linear vector transition" src="Images/cubicbezierlineartransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>