---
UID: NF:uianimation.IUIAnimationPriorityComparison.HasPriority
title: IUIAnimationPriorityComparison::HasPriority (uianimation.h)
description: Determines whether a new storyboard has priority over a scheduled storyboard.
helpviewer_keywords: ["HasPriority","HasPriority method [Windows Animation]","HasPriority method [Windows Animation]","IUIAnimationPriorityComparison interface","IUIAnimationPriorityComparison interface [Windows Animation]","HasPriority method","IUIAnimationPriorityComparison.HasPriority","IUIAnimationPriorityComparison::HasPriority","uianimation.iuianimationprioritycomparison_haspriority","uianimation/IUIAnimationPriorityComparison::HasPriority"]
old-location: uianimation\iuianimationprioritycomparison_haspriority.htm
tech.root: UIAnimation
ms.assetid: 82a90bd1-7bcf-4849-bad1-bae425169a2f
ms.date: 12/05/2018
ms.keywords: HasPriority, HasPriority method [Windows Animation], HasPriority method [Windows Animation],IUIAnimationPriorityComparison interface, IUIAnimationPriorityComparison interface [Windows Animation],HasPriority method, IUIAnimationPriorityComparison.HasPriority, IUIAnimationPriorityComparison::HasPriority, uianimation.iuianimationprioritycomparison_haspriority, uianimation/IUIAnimationPriorityComparison::HasPriority
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
 - IUIAnimationPriorityComparison::HasPriority
 - uianimation/IUIAnimationPriorityComparison::HasPriority
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
 - IUIAnimationPriorityComparison.HasPriority
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

A single animation variable can be included in multiple storyboards, but multiple storyboards cannot animate the same variable at the same time.
         
If a new storyboard attempts to animate one or more variables that are currently scheduled for animation by a different storyboard, a scheduling conflict occurs.
         
To determine which storyboard has priority, the animation manager can call <b>HasPriority</b> on one or more  priority comparison handlers provided by the application.

Registering priority comparison objects is optional.  By default, all storyboards can be trimmed, concluded or compressed to prevent failure, but none can be canceled, and by default no storyboards will be canceled or trimmed to prevent a delay.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>HasPriority</b>:

<ul>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstoryboardfromtag">IUIAnimationManager::GetStoryboardFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getvariablefromtag">IUIAnimationManager::GetVariableFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-gettag">IUIAnimationStoryboard::GetTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-gettag">IUIAnimationVariable::GetTag</a>
</li>
</ul>
<h3><a id="Contention_Management"></a><a id="contention_management"></a><a id="CONTENTION_MANAGEMENT"></a>Contention Management</h3>

To resolve a scheduling conflict, the animation manager has the following options:

<ul>
<li>Cancel the scheduled storyboard if it has not started playing and the priority comparison object registered with <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcancelprioritycomparison">IUIAnimationManager::SetCancelPriorityComparison</a> returns <b>S_OK</b>. Canceled storyboards are completely removed from the schedule.</li>
<li>Trim the scheduled storyboard if the priority comparison object registered with <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-settrimprioritycomparison">IUIAnimationManager::SetTrimPriorityComparison</a> returns <b>S_OK</b>. If the new storyboard trims the scheduled storyboard, the scheduled storyboard can no longer affect a variable when the new storyboard begins to animate that variable.</li>
<li>Conclude the scheduled storyboard if the scheduled storyboard contains a loop with a repetition count of <a href="/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a> and the priority comparison object registered with <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setconcludeprioritycomparison">IUIAnimationManager::SetConcludePriorityComparison</a> returns <b>S_OK</b>. If the storyboard is concluded, the current repetition of the loop completes, and the reminder of the storyboard then plays.</li>
<li>Compress the scheduled storyboard, and any other storyboards animating the same variables, if the priority comparison object registered with <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcompressprioritycomparison">IUIAnimationManager::SetCompressPriorityComparison</a>  returns <b>S_OK</b> for all scheduled storyboards that might be affected by the compression. When the storyboards are compressed, time is temporarily accelerated for affected storyboards, so they play faster.</li>
</ul>


If none of the above options is allowed by the priority comparison objects, the attempt to schedule the storyboard fails and Windows Animation returns <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_scheduling_result">UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY</a> to the calling application.

Note that for the new storyboard to be successfully scheduled, it must begin before its longest acceptable delay has elapsed.  This is determined by <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay">IUIAnimationStoryboard::SetLongestAcceptableDelay </a> or <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setdefaultlongestacceptabledelay">IUIAnimationManager::SetDefaultLongestAcceptableDelay </a>(if neither is called, the default is 0.0 seconds).  If the longest acceptable delay is <b>UI_ANIMATION_SECONDS_EVENTUALLY</b>, any finite delay will be sufficient.

The <i>priorityEffect</i> parameter describes the possible effect on the new storyboard if <b>HasPriority</b> were to return S_FALSE.  If <i>priorityEffect</i> is <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_priority_effect">UI_ANIMATION_PRIORITY_EFFECT_FAILURE</a>, it is possible that returning S_FALSE will result in a failure to schedule the new storyboard (it is also possible that the animation manager will be allowed to resolve the conflict in a different way by another priority comparison object).  If <i>priorityEffect</i> is <b>UI_ANIMATION_PRIORITY_EFFECT_DELAY</b>, the only downside of returning S_FALSE is that the storyboard might begin later than it would have had <i>HasPriority</i> returned S_OK.

When <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_priority_effect">UI_ANIMATION_PRIORITY_EFFECT_DELAY</a> is passed to <b>HasPriority</b>, the animation manager has already determined that it can schedule the new storyboard such that it will begin before its longest acceptable delay has elapsed, but it is in effect asking the application if the storyboard should begin even earlier.  In some scenarios, it might be best to reduce the latency of an animation by returning S_OK.  In others, it might be preferable to let scheduled animations complete whenever possible, in which case S_FALSE should be returned.  <b>UI_ANIMATION_PRIORITY_EFFECT_DELAY</b> is only passed to <b>HasPriority</b> when the animation manager is considering canceling or trimming a storyboard.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcancelprioritycomparison">IUIAnimationManager::SetCancelPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setcompressprioritycomparison">IUIAnimationManager::SetCompressPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setconcludeprioritycomparison">IUIAnimationManager::SetConcludePriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-settrimprioritycomparison">IUIAnimationManager::SetTrimPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationprioritycomparison">IUIAnimationPriorityComparison</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_priority_effect">UI_ANIMATION_PRIORITY_EFFECT</a>