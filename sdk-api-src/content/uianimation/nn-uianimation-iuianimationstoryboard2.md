---
UID: NN:uianimation.IUIAnimationStoryboard2
title: IUIAnimationStoryboard2 (uianimation.h)
description: Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.In this sectionTopicDescriptionAbandon MethodTerminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.AddKeyframeAfterTransition MethodAdds a keyframe at the end of the specified transition.AddKeyframeAtOffset MethodAdds a keyframe at the specified offset from an existing keyframe.AddTransition MethodAdds a transition to the storyboard.AddTransitionAtKeyframe MethodAdds a transition that starts at the specified keyframe.AddTransitionBetweenKeyframes MethodAdds a transition between two keyframes.Conclude MethodCompletes the current iteration of a keyframe loop that is in progress (where the loop is set to UI_ANIMATION_REPEAT_INDEFINITELY), terminates the loop, and continues with the storyboard. Finish MethodFinishes the storyboard within the specified time, compressing the storyboard if necessary.GetElapsedTime MethodGets the time that has elapsed since the storyboard started playing.GetStatus MethodGets the status of the storyboard.GetTag MethodGets the tag for a storyboard.HoldVariable MethodDirects the storyboard to hold the specified animation variable at its final value until the storyboard ends.RepeatBetweenKeyframes MethodCreates a loop between two keyframes.Schedule MethodDirects the storyboard to schedule itself for play.SetSkipDuration MethodSpecifies an offset from the beginning of a storyboard at which to start animating.SetLongestAcceptableDelay MethodSets the longest acceptable delay before the scheduled storyboard begins.SetStoryboardEventHandler MethodSpecifies a handler for storyboard events.SetTag MethodSets the tag for the storyboard. .helpviewer_keywords: ["IUIAnimationStoryboard2","IUIAnimationStoryboard2 interface [Windows Animation]","IUIAnimationStoryboard2 interface [Windows Animation]","described","uianimation.iuianimationstoryboard2","uianimation/IUIAnimationStoryboard2"]
old-location: uianimation\iuianimationstoryboard2.htm
tech.root: UIAnimation
ms.assetid: 507B6C2B-92C6-4AEB-82D5-3F14A332D41F
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard2, IUIAnimationStoryboard2 interface [Windows Animation], IUIAnimationStoryboard2 interface [Windows Animation],described, uianimation.iuianimationstoryboard2, uianimation/IUIAnimationStoryboard2
f1_keywords:
- uianimation/IUIAnimationStoryboard2
dev_langs:
- c++
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAnimation.dll
api_name:
- IUIAnimationStoryboard2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationStoryboard2 interface


## -description


Defines a storyboard, which contains a group of transitions
      that are synchronized relative to one another.<h2><a id="in_this_section"></a>In this section</h2>
<table>
<tr>
<th>Topic</th>
<th>Description</th>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-abandon">Abandon Method</a>


</td>
<td>
Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeaftertransition">AddKeyframeAfterTransition Method</a>


</td>
<td>
Adds a keyframe at the end of the specified transition.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeatoffset">AddKeyframeAtOffset Method</a>


</td>
<td>
Adds a keyframe at the specified offset from an existing keyframe.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransition">AddTransition Method</a>


</td>
<td>
Adds a transition to the storyboard.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionatkeyframe">AddTransitionAtKeyframe Method</a>


</td>
<td>
Adds a transition that starts at the specified keyframe.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionbetweenkeyframes">AddTransitionBetweenKeyframes Method</a>


</td>
<td>
Adds a transition between two keyframes.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-conclude">Conclude Method</a>


</td>
<td>
Completes the current iteration of a keyframe loop that is in progress (where the loop is set to <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a>), terminates the loop, and continues with the storyboard. 

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-finish">Finish Method</a>


</td>
<td>
Finishes the storyboard within the specified time, compressing the storyboard if necessary.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-getelapsedtime">GetElapsedTime Method</a>


</td>
<td>
Gets the time that has elapsed since the storyboard started playing.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-getstatus">GetStatus Method</a>


</td>
<td>
Gets the status of the storyboard.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-gettag">GetTag Method</a>


</td>
<td>
Gets the tag for a storyboard.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-holdvariable">HoldVariable Method</a>


</td>
<td>
Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-repeatbetweenkeyframes">RepeatBetweenKeyframes Method</a>


</td>
<td>
Creates a loop between two keyframes.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-schedule">Schedule Method</a>


</td>
<td>
Directs the storyboard to schedule itself for play.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-setskipduration">SetSkipDuration Method</a>


</td>
<td>
Specifies an offset from the beginning of a storyboard at which to start animating.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-setlongestacceptabledelay">SetLongestAcceptableDelay Method</a>


</td>
<td>
Sets the longest acceptable delay before the scheduled storyboard begins.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-setstoryboardeventhandler">SetStoryboardEventHandler Method</a>


</td>
<td>
Specifies a handler for storyboard events.

</td>
</tr>
<tr>
<td>

<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-settag">SetTag Method</a>


</td>
<td>
Sets the tag for the storyboard.

</td>
</tr>
</table>
 




## -members

The <b>IUIAnimationStoryboard2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-abandon">Abandon</a>
</td>
<td align="left" width="63%">
Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeaftertransition">AddKeyframeAfterTransition</a>
</td>
<td align="left" width="63%">
Adds a keyframe at the end of the specified transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeatoffset">AddKeyframeAtOffset</a>
</td>
<td align="left" width="63%">
Adds a keyframe at the specified offset from an existing keyframe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransition">AddTransition</a>
</td>
<td align="left" width="63%">
Adds a transition to the storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionatkeyframe">AddTransitionAtKeyframe</a>
</td>
<td align="left" width="63%">
Adds a transition that starts at the specified keyframe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionbetweenkeyframes">AddTransitionBetweenKeyframes</a>
</td>
<td align="left" width="63%">
Adds a transition between two keyframes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-conclude">Conclude</a>
</td>
<td align="left" width="63%">
Completes the current iteration of a keyframe loop that is in progress (where the loop is set to <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a>), terminates the loop, and continues with the storyboard. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-finish">Finish</a>
</td>
<td align="left" width="63%">
Finishes the storyboard within the specified time, compressing the storyboard if necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-getelapsedtime">GetElapsedTime</a>
</td>
<td align="left" width="63%">
Gets the time that has elapsed since the storyboard started playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag for a storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-holdvariable">HoldVariable</a>
</td>
<td align="left" width="63%">
Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-repeatbetweenkeyframes">RepeatBetweenKeyframes</a>
</td>
<td align="left" width="63%">
Creates a loop between two keyframes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-schedule">Schedule</a>
</td>
<td align="left" width="63%">
Directs the storyboard to schedule itself for play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-setlongestacceptabledelay">SetLongestAcceptableDelay</a>
</td>
<td align="left" width="63%">
Sets the longest acceptable delay before the scheduled storyboard begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-setskipduration">SetSkipDuration</a>
</td>
<td align="left" width="63%">
Specifies an offset from the beginning of a storyboard at which to start animating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-setstoryboardeventhandler">SetStoryboardEventHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for storyboard events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-settag">SetTag</a>
</td>
<td align="left" width="63%">
Sets the tag for the storyboard.

</td>
</tr>
</table>Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.

Adds a keyframe at the end of the specified transition.

Adds a keyframe at the specified offset from an existing keyframe.

Adds a transition to the storyboard.

Adds a transition that starts at the specified keyframe.

Adds a transition between two keyframes.

Completes the current iteration of a keyframe loop that is in progress (where the loop is set to <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a>), terminates the loop, and continues with the storyboard. 

Finishes the storyboard within the specified time, compressing the storyboard if necessary.

Gets the time that has elapsed since the storyboard started playing.

Gets the status of the storyboard.

Gets the tag for a storyboard.

Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.

Creates a loop between two keyframes.

Directs the storyboard to schedule itself for play.

Sets the longest acceptable delay before the scheduled storyboard begins.

Specifies an offset from the beginning of a storyboard at which to start animating.

Specifies a handler for storyboard events.

Sets the tag for the storyboard.

 

