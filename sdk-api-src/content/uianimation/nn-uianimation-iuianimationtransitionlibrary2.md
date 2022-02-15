---
UID: NN:uianimation.IUIAnimationTransitionLibrary2
title: IUIAnimationTransitionLibrary2 (uianimation.h)
description: Defines a library of standard transitions for a specified dimension.
helpviewer_keywords: ["IUIAnimationTransitionLibrary2","IUIAnimationTransitionLibrary2 interface [Windows Animation]","IUIAnimationTransitionLibrary2 interface [Windows Animation]","described","uianimation.iuianimationtransitionlibrary2","uianimation/IUIAnimationTransitionLibrary2"]
old-location: uianimation\iuianimationtransitionlibrary2.htm
tech.root: UIAnimation
ms.assetid: 92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransitionLibrary2, IUIAnimationTransitionLibrary2 interface [Windows Animation], IUIAnimationTransitionLibrary2 interface [Windows Animation],described, uianimation.iuianimationtransitionlibrary2, uianimation/IUIAnimationTransitionLibrary2
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
 - IUIAnimationTransitionLibrary2
 - uianimation/IUIAnimationTransitionLibrary2
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
 - IUIAnimationTransitionLibrary2
---

# IUIAnimationTransitionLibrary2 interface


## -description

Defines a library of standard transitions for a specified dimension.

## -inheritance

The <b>IUIAnimationTransitionLibrary2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTransitionLibrary2</b> also has these types of members:

## -remarks

Windows Animation includes a library of common transitions that developers can apply to variables through a storyboard. The parameters for specifying a transition depend on the type of transition. For some transitions, the duration of the transition is an explicit parameter; for others, the duration is determined by other parameters, such as speed or acceleration when the transition begins. A transition's initial value or velocity can be overridden if a discontinuous jump is desired, and duration can be queried after the transition is added to a storyboard.

If an application requires an effect that cannot be specified using the transition library, developers can implement custom transitions. A custom transition is created by first implementing the interpolator function for the transition, and then by using a factory object to generate transitions from interpolators. An interpolator must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a> interface; an implementation of the transition factory object is provided by the <a href="/previous-versions/windows/desktop/legacy/hh448667(v=vs.85)">UIAnimationTransitionFactory2</a> object.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-scheduletransition">IUIAnimationManager2::ScheduleTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransition">IUIAnimationStoryboard::AddTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/UIAnimation/-interfaces-main">Interfaces</a>



<a href="/windows/desktop/UIAnimation/storyboard-construction">Storyboard Overview</a>
