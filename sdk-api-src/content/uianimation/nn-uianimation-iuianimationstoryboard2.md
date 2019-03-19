---
UID: NN:uianimation.IUIAnimationStoryboard2
title: IUIAnimationStoryboard2 (uianimation.h)
author: windows-sdk-content
description: Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.In this sectionTopicDescriptionAbandon MethodTerminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.AddKeyframeAfterTransition MethodAdds a keyframe at the end of the specified transition.AddKeyframeAtOffset MethodAdds a keyframe at the specified offset from an existing keyframe.AddTransition MethodAdds a transition to the storyboard.AddTransitionAtKeyframe MethodAdds a transition that starts at the specified keyframe.AddTransitionBetweenKeyframes MethodAdds a transition between two keyframes.Conclude MethodCompletes the current iteration of a keyframe loop that is in progress (where the loop is set to UI_ANIMATION_REPEAT_INDEFINITELY), terminates the loop, and continues with the storyboard. Finish MethodFinishes the storyboard within the specified time, compressing the storyboard if necessary.GetElapsedTime MethodGets the time that has elapsed since the storyboard started playing.GetStatus MethodGets the status of the storyboard.GetTag MethodGets the tag for a storyboard.HoldVariable MethodDirects the storyboard to hold the specified animation variable at its final value until the storyboard ends.RepeatBetweenKeyframes MethodCreates a loop between two keyframes.Schedule MethodDirects the storyboard to schedule itself for play.SetSkipDuration MethodSpecifies an offset from the beginning of a storyboard at which to start animating.SetLongestAcceptableDelay MethodSets the longest acceptable delay before the scheduled storyboard begins.SetStoryboardEventHandler MethodSpecifies a handler for storyboard events.SetTag MethodSets the tag for the storyboard. .
old-location: uianimation\iuianimationstoryboard2.htm
tech.root: UIAnimation
ms.assetid: 507B6C2B-92C6-4AEB-82D5-3F14A332D41F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAnimationStoryboard2, IUIAnimationStoryboard2 interface [Windows Animation], IUIAnimationStoryboard2 interface [Windows Animation],described, uianimation.iuianimationstoryboard2, uianimation/IUIAnimationStoryboard2
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

<a href="https://msdn.microsoft.com/ABB7184F-A703-45E3-96D8-E3062EEB9565">Abandon Method</a>


</td>
<td>
Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/F5D13D36-1AEE-4D47-9683-A428E9ADF1D6">AddKeyframeAfterTransition Method</a>


</td>
<td>
Adds a keyframe at the end of the specified transition.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/6AB47BC1-4437-4191-8B66-8545EB4102A9">AddKeyframeAtOffset Method</a>


</td>
<td>
Adds a keyframe at the specified offset from an existing keyframe.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/BFC05D67-EE1C-489E-9A8C-10F0AAB24A0A">AddTransition Method</a>


</td>
<td>
Adds a transition to the storyboard.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/F4DAB833-E857-4FD8-87E2-8F32AF460F90">AddTransitionAtKeyframe Method</a>


</td>
<td>
Adds a transition that starts at the specified keyframe.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/55AEA5EA-7D9E-4669-8315-7A6F4428EDF9">AddTransitionBetweenKeyframes Method</a>


</td>
<td>
Adds a transition between two keyframes.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/C7687E52-433F-4E73-910D-86298E528F7B">Conclude Method</a>


</td>
<td>
Completes the current iteration of a keyframe loop that is in progress (where the loop is set to <a href="https://msdn.microsoft.com/09213B74-16C9-48F9-9626-59FF6CFDE975">UI_ANIMATION_REPEAT_INDEFINITELY</a>), terminates the loop, and continues with the storyboard. 

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/632BC77D-F2C5-4D08-8E9C-0598617A1DA7">Finish Method</a>


</td>
<td>
Finishes the storyboard within the specified time, compressing the storyboard if necessary.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/014F8A6A-345A-4DA7-8002-20A4683BB3B6">GetElapsedTime Method</a>


</td>
<td>
Gets the time that has elapsed since the storyboard started playing.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/1694B720-891A-4214-A009-6AA722E5B83D">GetStatus Method</a>


</td>
<td>
Gets the status of the storyboard.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/A73D5003-FC28-4A79-B157-3D0D2E0DEB3D">GetTag Method</a>


</td>
<td>
Gets the tag for a storyboard.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/E6B7C4F9-2377-4968-A16F-15F174EC5439">HoldVariable Method</a>


</td>
<td>
Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/31BC2628-14B3-4405-BA9B-4FB275D9AC0D">RepeatBetweenKeyframes Method</a>


</td>
<td>
Creates a loop between two keyframes.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/9F20AE4A-F693-4DDA-90F4-FCCA5291208B">Schedule Method</a>


</td>
<td>
Directs the storyboard to schedule itself for play.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/177623D7-5516-41EA-9014-61B150E527D9">SetSkipDuration Method</a>


</td>
<td>
Specifies an offset from the beginning of a storyboard at which to start animating.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/D23F4833-413C-470B-8572-2DCB051576A3">SetLongestAcceptableDelay Method</a>


</td>
<td>
Sets the longest acceptable delay before the scheduled storyboard begins.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/9C105DDC-4BED-45FC-B4AE-2331A228BB86">SetStoryboardEventHandler Method</a>


</td>
<td>
Specifies a handler for storyboard events.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/9BEB2BF7-55F7-43F7-822C-CB4AC6F29E32">SetTag Method</a>


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
<a href="https://msdn.microsoft.com/ABB7184F-A703-45E3-96D8-E3062EEB9565">Abandon</a>
</td>
<td align="left" width="63%">
Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F5D13D36-1AEE-4D47-9683-A428E9ADF1D6">AddKeyframeAfterTransition</a>
</td>
<td align="left" width="63%">
Adds a keyframe at the end of the specified transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6AB47BC1-4437-4191-8B66-8545EB4102A9">AddKeyframeAtOffset</a>
</td>
<td align="left" width="63%">
Adds a keyframe at the specified offset from an existing keyframe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BFC05D67-EE1C-489E-9A8C-10F0AAB24A0A">AddTransition</a>
</td>
<td align="left" width="63%">
Adds a transition to the storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F4DAB833-E857-4FD8-87E2-8F32AF460F90">AddTransitionAtKeyframe</a>
</td>
<td align="left" width="63%">
Adds a transition that starts at the specified keyframe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55AEA5EA-7D9E-4669-8315-7A6F4428EDF9">AddTransitionBetweenKeyframes</a>
</td>
<td align="left" width="63%">
Adds a transition between two keyframes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C7687E52-433F-4E73-910D-86298E528F7B">Conclude</a>
</td>
<td align="left" width="63%">
Completes the current iteration of a keyframe loop that is in progress (where the loop is set to <a href="https://msdn.microsoft.com/09213B74-16C9-48F9-9626-59FF6CFDE975">UI_ANIMATION_REPEAT_INDEFINITELY</a>), terminates the loop, and continues with the storyboard. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/632BC77D-F2C5-4D08-8E9C-0598617A1DA7">Finish</a>
</td>
<td align="left" width="63%">
Finishes the storyboard within the specified time, compressing the storyboard if necessary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/014F8A6A-345A-4DA7-8002-20A4683BB3B6">GetElapsedTime</a>
</td>
<td align="left" width="63%">
Gets the time that has elapsed since the storyboard started playing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1694B720-891A-4214-A009-6AA722E5B83D">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A73D5003-FC28-4A79-B157-3D0D2E0DEB3D">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag for a storyboard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E6B7C4F9-2377-4968-A16F-15F174EC5439">HoldVariable</a>
</td>
<td align="left" width="63%">
Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31BC2628-14B3-4405-BA9B-4FB275D9AC0D">RepeatBetweenKeyframes</a>
</td>
<td align="left" width="63%">
Creates a loop between two keyframes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9F20AE4A-F693-4DDA-90F4-FCCA5291208B">Schedule</a>
</td>
<td align="left" width="63%">
Directs the storyboard to schedule itself for play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D23F4833-413C-470B-8572-2DCB051576A3">SetLongestAcceptableDelay</a>
</td>
<td align="left" width="63%">
Sets the longest acceptable delay before the scheduled storyboard begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/177623D7-5516-41EA-9014-61B150E527D9">SetSkipDuration</a>
</td>
<td align="left" width="63%">
Specifies an offset from the beginning of a storyboard at which to start animating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9C105DDC-4BED-45FC-B4AE-2331A228BB86">SetStoryboardEventHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for storyboard events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9BEB2BF7-55F7-43F7-822C-CB4AC6F29E32">SetTag</a>
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

Completes the current iteration of a keyframe loop that is in progress (where the loop is set to <a href="https://msdn.microsoft.com/09213B74-16C9-48F9-9626-59FF6CFDE975">UI_ANIMATION_REPEAT_INDEFINITELY</a>), terminates the loop, and continues with the storyboard. 

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

 

