---
UID: NF:uianimation.IUIAnimationTransitionLibrary2.CreateCubicVectorTransition
title: IUIAnimationTransitionLibrary2::CreateCubicVectorTransition (uianimation.h)
description: Creates a cubic vector transition for each specified dimension.
helpviewer_keywords: ["CreateCubicVectorTransition","CreateCubicVectorTransition method [Windows Animation]","CreateCubicVectorTransition method [Windows Animation]","IUIAnimationTransitionLibrary2 interface","IUIAnimationTransitionLibrary2 interface [Windows Animation]","CreateCubicVectorTransition method","IUIAnimationTransitionLibrary2.CreateCubicVectorTransition","IUIAnimationTransitionLibrary2::CreateCubicVectorTransition","uianimation.iuianimationtransitionlibrary2_createcubicvectortransition","uianimation/IUIAnimationTransitionLibrary2::CreateCubicVectorTransition"]
old-location: uianimation\iuianimationtransitionlibrary2_createcubicvectortransition.htm
tech.root: UIAnimation
ms.assetid: 27671A90-611C-457A-8D2B-657256896CF4
ms.date: 12/05/2018
ms.keywords: CreateCubicVectorTransition, CreateCubicVectorTransition method [Windows Animation], CreateCubicVectorTransition method [Windows Animation],IUIAnimationTransitionLibrary2 interface, IUIAnimationTransitionLibrary2 interface [Windows Animation],CreateCubicVectorTransition method, IUIAnimationTransitionLibrary2.CreateCubicVectorTransition, IUIAnimationTransitionLibrary2::CreateCubicVectorTransition, uianimation.iuianimationtransitionlibrary2_createcubicvectortransition, uianimation/IUIAnimationTransitionLibrary2::CreateCubicVectorTransition
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
 - IUIAnimationTransitionLibrary2::CreateCubicVectorTransition
 - uianimation/IUIAnimationTransitionLibrary2::CreateCubicVectorTransition
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
 - IUIAnimationTransitionLibrary2.CreateCubicVectorTransition
---

# IUIAnimationTransitionLibrary2::CreateCubicVectorTransition


## -description

Creates a cubic vector transition for each specified dimension.

## -parameters

### -param duration [in]

The duration of the transition.

### -param finalValue [in]

A vector (of size <i>cDimension</i>) that contains  the final values of the animation variable at the end of the transition.

### -param finalVelocity [in]

A vector (of size <i>cDimension</i>) that contains  the final velocities (in units per second) of the animation variable at the end of the transition.

### -param cDimension [in]

The number of dimensions to apply the transition. This parameter specifies the number of values listed in <i>finalValue</i> and <i>finalVelocity</i>.

### -param transition [out]

The new cubic transition.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

During a cubic transition, the value of the animation variable changes from its initial value to the <i>finalValue</i> over the <i>duration</i> of the transition, ending at the <i>finalVelocity</i>.

The following figure shows the effect on an animation variable over time during a cubic transition.

<img alt="Diagram showing a cubic transition" src="Images/CubicTransition.png"/>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>