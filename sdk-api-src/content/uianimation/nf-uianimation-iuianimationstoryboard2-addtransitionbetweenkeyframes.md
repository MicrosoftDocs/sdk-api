---
UID: NF:uianimation.IUIAnimationStoryboard2.AddTransitionBetweenKeyframes
title: IUIAnimationStoryboard2::AddTransitionBetweenKeyframes
author: windows-sdk-content
description: Adds a transition between two keyframes.
old-location: uianimation\iuianimationstoryboard2_addtransitionbetweenkeyframes.htm
old-project: UIAnimation
ms.assetid: 55AEA5EA-7D9E-4669-8315-7A6F4428EDF9
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: AddTransitionBetweenKeyframes, AddTransitionBetweenKeyframes method [Windows Animation], AddTransitionBetweenKeyframes method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],AddTransitionBetweenKeyframes method, IUIAnimationStoryboard2.AddTransitionBetweenKeyframes, IUIAnimationStoryboard2::AddTransitionBetweenKeyframes, uianimation.iuianimationstoryboard2_addtransitionbetweenkeyframes, uianimation/IUIAnimationStoryboard2::AddTransitionBetweenKeyframes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationStoryboard2.AddTransitionBetweenKeyframes
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard2::AddTransitionBetweenKeyframes


## -description



   Adds a transition between two keyframes.


## -parameters




### -param variable [in]


                The animation variable for which the transition is to be added.


### -param transition [in]


               The transition to be added.


### -param startKeyframe [in]


               A keyframe that specifies the beginning of the new transition.


### -param endKeyframe [in]


               A keyframe that specifies the end of the new transition. It must not be possible for <i>endKeyframe</i> to appear earlier in the storyboard than <i>startKeyframe</i>.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_TRANSITION_ALREADY_USED</b></dt>
</dl>
</td>
<td width="60%">
This transition has already been added to a storyboard or has been added to a storyboard that has finished playing and been released.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_TRANSITION_ECLIPSED</b></dt>
</dl>
</td>
<td width="60%">
The transition might eclipse the beginning of another transition in the storyboard.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_START_KEYFRAME_AFTER_END</b></dt>
</dl>
</td>
<td width="60%">
The start keyframe might occur after the end keyframe.

</td>
</tr>
</table>
 

See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method applies the specified transition to the specified variable in the storyboard, with the transition starting and ending at the specified keyframes.  If the transition was created with a duration parameter specified, that duration is overwritten with the duration of time between the start and end keyframes. Otherwise, Windows Animation speeds up or slows down the transition as necessary.


         A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.

Transitions must be added in the order in which they will be played. A transition may begin playing before the preceding transition in the storyboard has finished, in which case the initial value and velocity seen by the new transition will be determined by the state of the preceding one. It must not be possible for a transition to begin before the start of the preceding transition.




## -see-also




<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/F5D13D36-1AEE-4D47-9683-A428E9ADF1D6">
      IUIAnimationStoryboard2::AddKeyframeAfterTransition</a>



<a href="https://msdn.microsoft.com/6AB47BC1-4437-4191-8B66-8545EB4102A9">
      IUIAnimationStoryboard2::AddKeyframeAtOffset</a>



<a href="https://msdn.microsoft.com/BFC05D67-EE1C-489E-9A8C-10F0AAB24A0A">
      IUIAnimationStoryboard2::AddTransition</a>



<a href="https://msdn.microsoft.com/F4DAB833-E857-4FD8-87E2-8F32AF460F90">
      IUIAnimationStoryboard2::AddTransitionAtKeyframe</a>



<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">
      IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">
      IUIAnimationTransitionLibrary2</a>
 

 

