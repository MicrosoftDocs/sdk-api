---
UID: NF:uianimation.IUIAnimationPriorityComparison.HasPriority
title: IUIAnimationPriorityComparison::HasPriority
author: windows-sdk-content
description: Determines whether a new storyboard has priority over a scheduled storyboard.
old-location: uianimation\iuianimationprioritycomparison_haspriority.htm
tech.root: UIAnimation
ms.assetid: 82a90bd1-7bcf-4849-bad1-bae425169a2f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: HasPriority, HasPriority method [Windows Animation], HasPriority method [Windows Animation],IUIAnimationPriorityComparison interface, IUIAnimationPriorityComparison interface [Windows Animation],HasPriority method, IUIAnimationPriorityComparison.HasPriority, IUIAnimationPriorityComparison::HasPriority, uianimation.iuianimationprioritycomparison_haspriority, uianimation/IUIAnimationPriorityComparison::HasPriority
ms.topic: method
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
 - IUIAnimationPriorityComparison.HasPriority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationPriorityComparison::HasPriority


## -description


Determines whether a new storyboard has priority over a scheduled storyboard.


## -parameters




### -param scheduledStoryboard [in]

The currently scheduled storyboard.


### -param newStoryboard [in]

The new storyboard that is interrupting the scheduled storyboard specified in <i>scheduledStoryboard</i>.


### -param priorityEffect [in]

 
					The potential effect on <i>newStoryboard</i> if <i>scheduledStoryboard</i> has a higher priority.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
<i>newStoryboard</i> has priority.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
<i>scheduledStoryboard</i> has priority.

</td>
</tr>
</table>
 




## -remarks



A single animation variable can be included in multiple storyboards, 
         but multiple storyboards cannot animate the same variable at the same time.
         
         If a new storyboard attempts to animate one or more variables that are currently scheduled for animation by a different storyboard, a scheduling conflict occurs.
         
         To determine which storyboard has priority, the animation manager can call <b>HasPriority</b> on one or more  priority comparison handlers provided by the application.

Registering priority comparison objects is optional.  By default, all storyboards can be trimmed, concluded or compressed to prevent failure, but none can be canceled, and by default no storyboards will be canceled or trimmed to prevent a delay.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>HasPriority</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/74a9265a-3602-4707-949e-6073cbde9ac4">IUIAnimationManager::GetStoryboardFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/611c5341-f225-461d-9718-a2432d796764">IUIAnimationManager::GetVariableFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c74dc23-ea42-400d-a78c-79b716c5e614">IUIAnimationStoryboard::GetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2731d302-dc52-4a10-8012-a246856d132b">IUIAnimationVariable::GetTag</a>
</li>
</ul>
<h3><a id="Contention_Management"></a><a id="contention_management"></a><a id="CONTENTION_MANAGEMENT"></a>Contention Management</h3>

To resolve a scheduling conflict, 
         the animation manager has the following options:

<ul>
<li>Cancel the scheduled storyboard if it has not started playing and the priority comparison object registered with <a href="https://msdn.microsoft.com/cea146d1-4a9c-4089-8015-ac16602f5afd">IUIAnimationManager::SetCancelPriorityComparison</a> returns <b>S_OK</b>. Canceled storyboards are completely removed from the schedule.</li>
<li>Trim the scheduled storyboard if the priority comparison object registered with <a href="https://msdn.microsoft.com/f4c81cc4-4c00-4f78-819d-55f79972fe46">IUIAnimationManager::SetTrimPriorityComparison</a> returns <b>S_OK</b>. If the new storyboard trims the scheduled storyboard, the scheduled storyboard can no longer affect a variable when the new storyboard begins to animate that variable.</li>
<li>Conclude the scheduled storyboard if the scheduled storyboard contains a loop with a repetition count of <a href="https://msdn.microsoft.com/09213B74-16C9-48F9-9626-59FF6CFDE975">UI_ANIMATION_REPEAT_INDEFINITELY</a> and the priority comparison object registered with <a href="https://msdn.microsoft.com/00a3d7e4-7ad2-46a8-a9c2-0e725005c00b">IUIAnimationManager::SetConcludePriorityComparison</a> returns <b>S_OK</b>. If the storyboard is concluded, the current repetition of the loop completes, and the reminder of the storyboard then plays.</li>
<li>Compress the scheduled storyboard, and any other storyboards animating the same variables, if the priority comparison object registered with
            <a href="https://msdn.microsoft.com/bf2a7782-3541-483e-8d5e-3e82693f103c">IUIAnimationManager::SetCompressPriorityComparison</a>  returns <b>S_OK</b> for all scheduled storyboards that might be affected by the compression. When the storyboards are compressed, time is temporarily accelerated for affected storyboards, so they play faster.</li>
</ul>


If none of the above options is allowed by the priorty comparison objects, the attempt to schedule the storyboard fails and Windows Animation returns <a href="https://msdn.microsoft.com/en-us/library/Dd371967(v=VS.85).aspx">UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY</a> to the calling application.

Note that for the new storyboard to be successfully scheduled, it must begin before its longest acceptable delay has elapsed.  This is determined by <a href="https://msdn.microsoft.com/5f87a4b1-8db9-42ba-963f-664db588c520">IUIAnimationStoryboard::SetLongestAcceptableDelay </a>or <a href="https://msdn.microsoft.com/27182009-1614-41a0-9b55-7c1dcb494883">IUIAnimationManager::SetDefaultLongestAcceptableDelay </a>(if neither is called, the default is 0.0 seconds).  If the longest acceptable delay is <b>UI_ANIMATION_SECONDS_EVENTUALLY</b>, any finite delay will be sufficient.

The <i>priorityEffect</i> parameter describes the possible effect on the new storyboard if <b>HasPriority</b> were to return S_FALSE.  If <i>priorityEffect</i> is <a href="https://msdn.microsoft.com/en-us/library/Dd317049(v=VS.85).aspx">UI_ANIMATION_PRIORITY_EFFECT_FAILURE</a>, it is possible that returning S_FALSE will result in a failure to schedule the new storyboard (it is also possible that the animation manager will be allowed to resolve the conflict in a different way by another priority comparison object).  If <i>priorityEffect</i> is <b>UI_ANIMATION_PRIORITY_EFFECT_DELAY</b>, the only downside of returning S_FALSE is that the storyboard might begin later than it would have had <i>HasPriority</i> returned S_OK.

When <a href="https://msdn.microsoft.com/en-us/library/Dd317049(v=VS.85).aspx">UI_ANIMATION_PRIORITY_EFFECT_DELAY</a> is passed to <b>HasPriority</b>, the animation manager has already determined that it can schedule the new storyboard such that it will begin before its longest acceptable delay has elapsed, but it is in effect asking the application if the storyboard should begin even earlier.  In some scenarios, it might be best to reduce the latency of an animation by returning S_OK.  In others, it might be preferable to let scheduled animations complete whenever possible, in which case S_FALSE should be returned.  <b>UI_ANIMATION_PRIORITY_EFFECT_DELAY</b> is only passed to <b>HasPriority</b> when the animation manager is considering canceling or trimming a storyboard.




## -see-also




<a href="https://msdn.microsoft.com/cea146d1-4a9c-4089-8015-ac16602f5afd">IUIAnimationManager::SetCancelPriorityComparison</a>



<a href="https://msdn.microsoft.com/bf2a7782-3541-483e-8d5e-3e82693f103c">IUIAnimationManager::SetCompressPriorityComparison</a>



<a href="https://msdn.microsoft.com/00a3d7e4-7ad2-46a8-a9c2-0e725005c00b">IUIAnimationManager::SetConcludePriorityComparison</a>



<a href="https://msdn.microsoft.com/f4c81cc4-4c00-4f78-819d-55f79972fe46">IUIAnimationManager::SetTrimPriorityComparison</a>



<a href="https://msdn.microsoft.com/65311cf0-f8d4-4d2c-bd4d-585ae5d921df">IUIAnimationPriorityComparison</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd317049(v=VS.85).aspx">UI_ANIMATION_PRIORITY_EFFECT</a>
 

 

