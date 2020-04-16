---
UID: NN:uianimation.IUIAnimationTransitionLibrary2
title: IUIAnimationTransitionLibrary2 (uianimation.h)
description: Defines a library of standard transitions for a specified dimension.helpviewer_keywords: ["IUIAnimationTransitionLibrary2","IUIAnimationTransitionLibrary2 interface [Windows Animation]","IUIAnimationTransitionLibrary2 interface [Windows Animation]","described","uianimation.iuianimationtransitionlibrary2","uianimation/IUIAnimationTransitionLibrary2"]
old-location: uianimation\iuianimationtransitionlibrary2.htm
tech.root: UIAnimation
ms.assetid: 92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransitionLibrary2, IUIAnimationTransitionLibrary2 interface [Windows Animation], IUIAnimationTransitionLibrary2 interface [Windows Animation],described, uianimation.iuianimationtransitionlibrary2, uianimation/IUIAnimationTransitionLibrary2
f1_keywords:
- uianimation/IUIAnimationTransitionLibrary2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAnimation.dll
api_name:
- IUIAnimationTransitionLibrary2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTransitionLibrary2 interface


## -description


Defines a library of standard transitions for a specified dimension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTransitionLibrary2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTransitionLibrary2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationTransitionLibrary2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createacceleratedeceleratetransition">CreateAccelerateDecelerateTransition</a>
</td>
<td align="left" width="63%">
Creates an accelerate-decelerate scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createconstanttransition">CreateConstantTransition</a>
</td>
<td align="left" width="63%">
Creates a constant scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createcubicbezierlineartransition">CreateCubicBezierLinearTransition</a>
</td>
<td align="left" width="63%">
Creates a cubic Bézier linear scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createcubicbezierlinearvectortransition">CreateCubicBezierLinearVectorTransition</a>
</td>
<td align="left" width="63%">
Creates a cubic Bézier linear vector transition for each specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createcubictransition">CreateCubicTransition</a>
</td>
<td align="left" width="63%">
Creates a cubic scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createcubicvectortransition">CreateCubicVectorTransition</a>
</td>
<td align="left" width="63%">
Creates a cubic vector transition for each specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-creatediscretetransition">CreateDiscreteTransition</a>
</td>
<td align="left" width="63%">
Creates a discrete scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-creatediscretevectortransition">CreateDiscreteVectorTransition</a>
</td>
<td align="left" width="63%">
Creates a discrete vector transition for each specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createinstantaneoustransition">CreateInstantaneousTransition</a>
</td>
<td align="left" width="63%">
Creates an instantaneous scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createinstantaneousvectortransition">CreateInstantaneousVectorTransition</a>
</td>
<td align="left" width="63%">
Creates an instantaneous vector transition for each specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createlineartransition">CreateLinearTransition</a>
</td>
<td align="left" width="63%">
Creates a linear scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createlineartransitionfromspeed">CreateLinearTransitionFromSpeed</a>
</td>
<td align="left" width="63%">
Creates a linear-speed scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createlinearvectortransition">CreateLinearVectorTransition</a>
</td>
<td align="left" width="63%">
Creates a linear vector transition in the specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createlinearvectortransitionfromspeed">CreateLinearVectorTransitionFromSpeed</a>
</td>
<td align="left" width="63%">
Creates a linear-speed vector transition in the specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createparabolictransitionfromacceleration">CreateParabolicTransitionFromAcceleration</a>
</td>
<td align="left" width="63%">
Creates a parabolic-acceleration scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createreversaltransition">CreateReversalTransition</a>
</td>
<td align="left" width="63%">
Creates a reversal scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createsinusoidaltransitionfromrange">CreateSinusoidalTransitionFromRange</a>
</td>
<td align="left" width="63%">
Creates a sinusoidal-range scalar  transition with a specified range of oscillation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createsinusoidaltransitionfromvelocity">CreateSinusoidalTransitionFromVelocity</a>
</td>
<td align="left" width="63%">
Creates a sinusoidal scalar transition where amplitude is determined by initial velocity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary2-createsmoothstoptransition">CreateSmoothStopTransition</a>
</td>
<td align="left" width="63%">
Creates a smooth-stop scalar transition.

</td>
</tr>
</table> 


## -remarks



Windows Animation includes a library of common transitions that developers can apply to variables through a storyboard. The parameters for specifying a transition depend on the type of transition. For some transitions, the duration of the transition is an explicit parameter; for others, the duration is determined by other parameters, such as speed or acceleration when the transition begins. A transition's initial value or velocity can be overridden if a discontinuous jump is desired, and duration can be queried after the transition is added to a storyboard.

If an application requires an effect that cannot be specified using the transition library, developers can implement custom transitions. A custom transition is created by first implementing the interpolator function for the transition, and then by using a factory object to generate transitions from interpolators. An interpolator must implement the <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a>interface; an implementation of the transition factory object is provided by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh448667(v=vs.85)">UIAnimationTransitionFactory2</a> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-scheduletransition">IUIAnimationManager2::ScheduleTransition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransition">IUIAnimationStoryboard::AddTransition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/UIAnimation/-interfaces-main">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/UIAnimation/storyboard-construction">Storyboard Overview</a>
 

 

