---
UID: NN:uianimation.IUIAnimationTransitionLibrary
title: IUIAnimationTransitionLibrary (uianimation.h)
description: Defines a library of standard transitions.
helpviewer_keywords: ["IUIAnimationTransitionLibrary","IUIAnimationTransitionLibrary interface [Windows Animation]","IUIAnimationTransitionLibrary interface [Windows Animation]","described","uianimation.iuianimationtransitionlibrary","uianimation/IUIAnimationTransitionLibrary"]
old-location: uianimation\iuianimationtransitionlibrary.htm
tech.root: UIAnimation
ms.assetid: 7d256937-b191-499f-9711-05a5ef3b8e18
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransitionLibrary, IUIAnimationTransitionLibrary interface [Windows Animation], IUIAnimationTransitionLibrary interface [Windows Animation],described, uianimation.iuianimationtransitionlibrary, uianimation/IUIAnimationTransitionLibrary
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps \| UWP apps]
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
 - IUIAnimationTransitionLibrary
 - uianimation/IUIAnimationTransitionLibrary
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
 - IUIAnimationTransitionLibrary
---

# IUIAnimationTransitionLibrary interface


## -description

Defines a library of standard transitions.

## -inheritance

The <b>IUIAnimationTransitionLibrary</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTransitionLibrary</b> also has these types of members:

## -remarks

Windows Animation includes a library of common transitions that developers can apply to variables through a storyboard. The parameters for specifying a transition depend on the type of transition. For some transitions, the duration of the transition is an explicit parameter; for others, the duration is determined by other parameters, such as speed or acceleration when the transition begins. A transition's initial value or velocity can be overridden if a discontinuous jump is desired, and duration can be queried after the transition is added to a storyboard.

If an application requires an effect that cannot be specified using the transition library, developers can implement custom transitions. A custom transition is created by first implementing the interpolator function for the transition, and then by using a factory object to generate transitions from interpolators. An interpolator must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a> interface; an implementation of the transition factory object is provided by <a href="/previous-versions/windows/desktop/legacy/dd317024(v=vs.85)">UIAnimationTransitionFactory</a>.


#### Examples

For an example that creates the transition library object, see <a href="/windows/desktop/UIAnimation/adding-animation-to-an-application">Create the Main Animation Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-scheduletransition">IUIAnimationManager::ScheduleTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransition">IUIAnimationStoryboard::AddTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/UIAnimation/storyboard-construction">Storyboard Overview</a>
