---
UID: NN:uianimation.IUIAnimationTransitionLibrary2
title: IUIAnimationTransitionLibrary2
author: windows-sdk-content
description: Defines a library of standard transitions for a specified dimension.
old-location: uianimation\iuianimationtransitionlibrary2.htm
old-project: UIAnimation
ms.assetid: 92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationTransitionLibrary2, IUIAnimationTransitionLibrary2 interface [Windows Animation], IUIAnimationTransitionLibrary2 interface [Windows Animation],described, uianimation.iuianimationtransitionlibrary2, uianimation/IUIAnimationTransitionLibrary2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps | UWP apps]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTransitionLibrary2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary2 interface


## -description


Defines a library of standard transitions for a specified dimension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTransitionLibrary2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationTransitionLibrary2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/813B4539-2942-484E-BC20-3A8178EBF9A0">CreateAccelerateDecelerateTransition</a>
</td>
<td align="left" width="63%">

      Creates an accelerate-decelerate scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CC7315BB-B3EC-4B40-85B9-1AF70ABB5F77">CreateConstantTransition</a>
</td>
<td align="left" width="63%">

      Creates a constant scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1943D3B6-0DA6-4F1B-B52D-F121BAC6BE68">CreateCubicBezierLinearTransition</a>
</td>
<td align="left" width="63%">

      Creates a cubic Bézier linear scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AA1630D4-7E8B-4B1D-B3F8-1BDB9C3F73C7">CreateCubicBezierLinearVectorTransition</a>
</td>
<td align="left" width="63%">

      Creates a cubic Bézier linear vector transition for each specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63ADBD53-2552-4D68-AABD-E3B1F83831EB">CreateCubicTransition</a>
</td>
<td align="left" width="63%">

      Creates a cubic scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27671A90-611C-457A-8D2B-657256896CF4">CreateCubicVectorTransition</a>
</td>
<td align="left" width="63%">

      Creates a cubic vector transition for each specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1BDF8ED9-C39D-4FEF-A335-B3BE4EAAD297">CreateDiscreteTransition</a>
</td>
<td align="left" width="63%">

      Creates a discrete scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8580FED2-7F39-4EA8-B2C5-CDB887121359">CreateDiscreteVectorTransition</a>
</td>
<td align="left" width="63%">

      Creates a discrete vector transition for each specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E40313C5-F98E-4BF3-83B8-735271ED1E2C">CreateInstantaneousTransition</a>
</td>
<td align="left" width="63%">

      Creates an instantaneous scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C4E97F25-85BD-4548-950D-06BD5E6C4831">CreateInstantaneousVectorTransition</a>
</td>
<td align="left" width="63%">

      Creates an instantaneous vector transition for each specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BD0A9D4E-0306-4C76-8CC2-AA1A747C4538">CreateLinearTransition</a>
</td>
<td align="left" width="63%">

      Creates a linear scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BCB9D6C6-6EFE-4CDF-8239-9E7E07AB53BD">CreateLinearTransitionFromSpeed</a>
</td>
<td align="left" width="63%">

      Creates a linear-speed scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71A009AB-FBF3-4624-9B78-45C42B0CEE62">CreateLinearVectorTransition</a>
</td>
<td align="left" width="63%">

      Creates a linear vector transition in the specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5CFA1E23-26A7-4139-B533-8BD325E9F1B9">CreateLinearVectorTransitionFromSpeed</a>
</td>
<td align="left" width="63%">

      Creates a linear-speed vector transition in the specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C2005144-CA40-4835-8AFA-7E87AE99867F">CreateParabolicTransitionFromAcceleration</a>
</td>
<td align="left" width="63%">

      Creates a parabolic-acceleration scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49ECB93E-C253-4A7D-8181-8ED018520391">CreateReversalTransition</a>
</td>
<td align="left" width="63%">

      Creates a reversal scalar transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E4222165-4726-4C79-94A8-3CC2C72CCE42">CreateSinusoidalTransitionFromRange</a>
</td>
<td align="left" width="63%">

      Creates a sinusoidal-range scalar  transition with a specified range of oscillation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/833D3482-68BC-45DD-9073-B048E11CB801">CreateSinusoidalTransitionFromVelocity</a>
</td>
<td align="left" width="63%">

      Creates a sinusoidal scalar transition where amplitude is determined by initial velocity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/011FFBF8-31A9-4253-B034-5836B7B74409">CreateSmoothStopTransition</a>
</td>
<td align="left" width="63%">

      Creates a smooth-stop scalar transition.

</td>
</tr>
</table> 


## -remarks



Windows Animation includes a library of common transitions that developers can apply to variables through a storyboard. The parameters for specifying a transition depend on the type of transition. For some transitions, the duration of the transition is an explicit parameter; for others, the duration is determined by other parameters, such as speed or acceleration when the transition begins. A transition's initial value or velocity can be overridden if a discontinuous jump is desired, and duration can be queried after the transition is added to a storyboard.

If an application requires an effect that cannot be specified using the transition library, developers can implement custom transitions. A custom transition is created by first implementing the interpolator function for the transition, and then by using a factory object to generate transitions from interpolators. An interpolator must implement the <a href="https://msdn.microsoft.com/EC0D1933-37C3-41E2-AB13-DA4AAF4B8F04">IUIAnimationInterpolator2</a>
 interface; an implementation of the transition factory object is provided by the <a href="https://msdn.microsoft.com/4583920B-FF11-48C8-B311-66F5DE3F9D9C">UIAnimationTransitionFactory2</a> object.




## -see-also




<a href="https://msdn.microsoft.com/F0F5D099-6290-485F-AD68-101CD57E8656">
      IUIAnimationManager2::ScheduleTransition</a>



<a href="https://msdn.microsoft.com/055206d8-ea9e-4013-89ee-2929bfeb2731">
      IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="https://msdn.microsoft.com/c3213e5d-c8f5-406a-bc44-9de7a740b070">
      IUIAnimationStoryboard::AddTransition</a>



<a href="https://msdn.microsoft.com/94a9aafc-fe5a-49a8-8e14-9e7c4624869a">
      IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="https://msdn.microsoft.com/75db41ef-526b-40aa-a62d-a4262cc8d80e">
      IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">
      IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/d37718ac-0256-4a24-a26c-d29173593be0">Storyboard Overview</a>
 

 

