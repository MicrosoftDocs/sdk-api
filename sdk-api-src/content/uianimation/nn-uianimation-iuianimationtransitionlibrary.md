---
UID: NN:uianimation.IUIAnimationTransitionLibrary
title: IUIAnimationTransitionLibrary (uianimation.h)
author: windows-sdk-content
description: Defines a library of standard transitions.
old-location: uianimation\iuianimationtransitionlibrary.htm
tech.root: UIAnimation
ms.assetid: 7d256937-b191-499f-9711-05a5ef3b8e18
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransitionLibrary, IUIAnimationTransitionLibrary interface [Windows Animation], IUIAnimationTransitionLibrary interface [Windows Animation],described, uianimation.iuianimationtransitionlibrary, uianimation/IUIAnimationTransitionLibrary
ms.topic: interface
f1_keywords: 
 - "uianimation/IUIAnimationTransitionLibrary"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationTransitionLibrary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationTransitionLibrary interface


## -description


Defines a library of standard transitions.
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTransitionLibrary</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTransitionLibrary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationTransitionLibrary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition">CreateAccelerateDecelerateTransition</a>
</td>
<td align="left" width="63%">
Creates an accelerate-decelerate transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-createconstanttransition">CreateConstantTransition</a>
</td>
<td align="left" width="63%">
Creates a constant transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-createcubictransition">CreateCubicTransition</a>
</td>
<td align="left" width="63%">
Creates a cubic transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-creatediscretetransition">CreateDiscreteTransition</a>
</td>
<td align="left" width="63%">
Creates a discrete transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-createinstantaneoustransition">CreateInstantaneousTransition</a>
</td>
<td align="left" width="63%">
Creates an instantaneous transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition">CreateLinearTransition</a>
</td>
<td align="left" width="63%">
Creates a linear transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed">CreateLinearTransitionFromSpeed</a>
</td>
<td align="left" width="63%">
Creates a linear-speed transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-createparabolictransitionfromacceleration">CreateParabolicTransitionFromAcceleration</a>
</td>
<td align="left" width="63%">
Creates a parabolic-acceleration transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-createreversaltransition">CreateReversalTransition</a>
</td>
<td align="left" width="63%">
Creates a reversal transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-createsinusoidaltransitionfromrange">CreateSinusoidalTransitionFromRange</a>
</td>
<td align="left" width="63%">
Creates a sinusoidal-range transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-createsinusoidaltransitionfromvelocity">CreateSinusoidalTransitionFromVelocity</a>
</td>
<td align="left" width="63%">
Creates a sinusoidal-velocity transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransitionlibrary-createsmoothstoptransition">CreateSmoothStopTransition</a>
</td>
<td align="left" width="63%">
Creates a smooth-stop transition.

</td>
</tr>
</table> 


## -remarks



Windows Animation includes a library of common transitions that developers can apply to variables through a storyboard. The parameters for specifying a transition depend on the type of transition. For some transitions, the duration of the transition is an explicit parameter; for others, the duration is determined by other parameters, such as speed or acceleration when the transition begins. A transition's initial value or velocity can be overridden if a discontinuous jump is desired, and duration can be queried after the transition is added to a storyboard.

If an application requires an effect that cannot be specified using the transition library, developers can implement custom transitions. A custom transition is created by first implementing the interpolator function for the transition, and then by using a factory object to generate transitions from interpolators. An interpolator must implement the <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator">IUIAnimationInterpolator</a>interface; an implementation of the transition factory object is provided by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd317024(v=vs.85)">UIAnimationTransitionFactory</a>.


#### Examples

For an example that creates the transition library object, see <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/adding-animation-to-an-application">Create the Main Animation Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-scheduletransition">IUIAnimationManager::ScheduleTransition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransition">IUIAnimationStoryboard::AddTransition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/UIAnimation/storyboard-construction">Storyboard Overview</a>
 

 

