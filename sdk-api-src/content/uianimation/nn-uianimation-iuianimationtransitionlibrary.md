---
UID: NN:uianimation.IUIAnimationTransitionLibrary
title: IUIAnimationTransitionLibrary
author: windows-driver-content
description: Defines a library of standard transitions.
old-location: uianimation\iuianimationtransitionlibrary.htm
old-project: UIAnimation
ms.assetid: 7d256937-b191-499f-9711-05a5ef3b8e18
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IUIAnimationTransitionLibrary, IUIAnimationTransitionLibrary interface [Windows Animation], IUIAnimationTransitionLibrary interface [Windows Animation],described, uianimation.iuianimationtransitionlibrary, uianimation/IUIAnimationTransitionLibrary
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps | UWP apps]
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationTransitionLibrary
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationTransitionLibrary interface


## -description



      Defines a library of standard transitions.
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTransitionLibrary</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationTransitionLibrary</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/97a0c6cc-991b-464f-b000-1d1199c5f4de">
         CreateAccelerateDecelerateTransition</a>
</td>
<td align="left" width="63%">

         Creates an accelerate-decelerate transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9ad2c2d-8bcd-4730-86da-9b9432ac5b93">
         CreateConstantTransition</a>
</td>
<td align="left" width="63%">

         Creates a constant transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5003685d-d4d7-4871-b700-4d7f38050ada">
         CreateCubicTransition</a>
</td>
<td align="left" width="63%">

         Creates a cubic transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c3f6ccb-7a42-4a48-90ad-dba99c67aa6f">
         CreateDiscreteTransition</a>
</td>
<td align="left" width="63%">

         Creates a discrete transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70db1315-df4a-472e-8d79-61bf93980337">
         CreateInstantaneousTransition</a>
</td>
<td align="left" width="63%">

         Creates an instantaneous transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51c54bc9-771c-484e-a24f-22ba03c70709">
         CreateLinearTransition</a>
</td>
<td align="left" width="63%">

         Creates a linear transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f9ce1c0-8681-456d-8ab5-76214dc529ba">
         CreateLinearTransitionFromSpeed</a>
</td>
<td align="left" width="63%">

         Creates a linear-speed transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96dd5287-36b1-4620-88ae-a52b252620d2">
         CreateParabolicTransitionFromAcceleration</a>
</td>
<td align="left" width="63%">

         Creates a parabolic-acceleration transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca1d0551-333f-4fe1-b288-5ccce846d697">
         CreateReversalTransition</a>
</td>
<td align="left" width="63%">

         Creates a reversal transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7164bcac-3de3-4b52-8eb3-d38156573feb">
         CreateSinusoidalTransitionFromRange</a>
</td>
<td align="left" width="63%">

         Creates a sinusoidal-range transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47998787-dcd5-4973-bf7e-30096b01c51b">
         CreateSinusoidalTransitionFromVelocity</a>
</td>
<td align="left" width="63%">

         Creates a sinusoidal-velocity transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fce15425-5529-4ebf-9961-7e125cc64edb">
         CreateSmoothStopTransition</a>
</td>
<td align="left" width="63%">

         Creates a smooth-stop transition.

</td>
</tr>
</table> 


## -remarks



Windows Animation includes a library of common transitions that developers can apply to variables through a storyboard. The parameters for specifying a transition depend on the type of transition. For some transitions, the duration of the transition is an explicit parameter; for others, the duration is determined by other parameters, such as speed or acceleration when the transition begins. A transition's initial value or velocity can be overridden if a discontinuous jump is desired, and duration can be queried after the transition is added to a storyboard.

If an application requires an effect that cannot be specified using the transition library, developers can implement custom transitions. A custom transition is created by first implementing the interpolator function for the transition, and then by using a factory object to generate transitions from interpolators. An interpolator must implement the <a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a>
 interface; an implementation of the transition factory object is provided by <a href="https://msdn.microsoft.com/27749b03-e993-42bf-855d-4fe352a1bb8e">UIAnimationTransitionFactory</a>.


#### Examples

For an example that creates the transition library object, see <a href="https://msdn.microsoft.com/4005819e-482c-4052-89f8-b8e457c0c3dc">Create the Main Animation Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0178b674-2ad3-49ee-92ce-925840ab8409">
      IUIAnimationManager::ScheduleTransition</a>



<a href="https://msdn.microsoft.com/055206d8-ea9e-4013-89ee-2929bfeb2731">
      IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="https://msdn.microsoft.com/c3213e5d-c8f5-406a-bc44-9de7a740b070">
      IUIAnimationStoryboard::AddTransition</a>



<a href="https://msdn.microsoft.com/94a9aafc-fe5a-49a8-8e14-9e7c4624869a">
      IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="https://msdn.microsoft.com/75db41ef-526b-40aa-a62d-a4262cc8d80e">
      IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">
      IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/d37718ac-0256-4a24-a26c-d29173593be0">Storyboard Overview</a>
 

 

