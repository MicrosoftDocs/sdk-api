---
UID: NF:uianimation.IUIAnimationPriorityComparison2.HasPriority
title: IUIAnimationPriorityComparison2::HasPriority (uianimation.h)
description: Determines the relative priority between a scheduled storyboard and a new storyboard.
helpviewer_keywords: ["HasPriority","HasPriority method [Windows Animation]","HasPriority method [Windows Animation]","IUIAnimationPriorityComparison2 interface","IUIAnimationPriorityComparison2 interface [Windows Animation]","HasPriority method","IUIAnimationPriorityComparison2.HasPriority","IUIAnimationPriorityComparison2::HasPriority","uianimation.iuianimationprioritycomparison2_haspriority","uianimation/IUIAnimationPriorityComparison2::HasPriority"]
old-location: uianimation\iuianimationprioritycomparison2_haspriority.htm
tech.root: UIAnimation
ms.assetid: A448144F-37B2-46E5-AA0D-604CE3FDEAA4
ms.date: 12/05/2018
ms.keywords: HasPriority, HasPriority method [Windows Animation], HasPriority method [Windows Animation],IUIAnimationPriorityComparison2 interface, IUIAnimationPriorityComparison2 interface [Windows Animation],HasPriority method, IUIAnimationPriorityComparison2.HasPriority, IUIAnimationPriorityComparison2::HasPriority, uianimation.iuianimationprioritycomparison2_haspriority, uianimation/IUIAnimationPriorityComparison2::HasPriority
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationPriorityComparison2::HasPriority
 - uianimation/IUIAnimationPriorityComparison2::HasPriority
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
 - IUIAnimationPriorityComparison2.HasPriority
---

# IUIAnimationPriorityComparison2::HasPriority


## -description

Determines the relative priority between a scheduled storyboard and a new storyboard.

## -parameters

### -param scheduledStoryboard [in]

The currently scheduled storyboard.

### -param newStoryboard [in]

The new storyboard that is interrupting the scheduled storyboard specified by <i>scheduledStoryboard</i>.

### -param priorityEffect [in]

 The potential effect on <i>newStoryboard</i> if <i>scheduledStoryboard</i> has a higher priority.

## -returns

Returns the following if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

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
         
To determine which storyboard has priority, the animation manager can call the <b>HasPriority</b> method on one or more  priority comparison handlers provided by the application.

Registering priority comparison objects is optional.  By default, all storyboards can be trimmed, concluded, or compressed to prevent failure, but none can be canceled, and by default no storyboards will be canceled or trimmed to prevent a delay.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationprioritycomparison-haspriority">HasPriority</a>:

<ul>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getstoryboardfromtag">IUIAnimationManager2::GetStoryboardFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getvariablefromtag">IUIAnimationManager2::GetVariableFromTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-gettag">IUIAnimationStoryboard::GetTag</a>
</li>
<li>
<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-gettag">IUIAnimationVariable2::GetTag</a>
</li>
</ul>
<h3><a id="Contention_Management"></a><a id="contention_management"></a><a id="CONTENTION_MANAGEMENT"></a>Contention Management</h3>

To resolve a scheduling conflict, the animation manager has the following options:

<ul>
<li>Cancel the scheduled storyboard if it has not started playing and the priority comparison object that is registered with <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setcancelprioritycomparison">IUIAnimationManager2::SetCancelPriorityComparison</a> returns <b>S_OK</b>. Canceled storyboards are completely removed from the schedule.</li>
<li>Trim the scheduled storyboard if the priority comparison object that is registered with <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-settrimprioritycomparison">IUIAnimationManager2::SetTrimPriorityComparison</a> returns <b>S_OK</b>. If the new storyboard trims the scheduled storyboard, the scheduled storyboard can no longer affect a variable when the new storyboard begins to animate that variable.</li>
<li>Conclude the scheduled storyboard if the scheduled storyboard contains a loop with a repetition count of <a href="/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a> and the priority comparison object that is registered with <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setconcludeprioritycomparison">IUIAnimationManager2::SetConcludePriorityComparison</a> returns <b>S_OK</b>. If the storyboard is concluded, the current repetition of the loop completes, and the reminder of the storyboard then plays.</li>
<li>Compress the scheduled storyboard, and any other storyboards animating the same variables, if the priority comparison object that is registered with <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setcompressprioritycomparison">IUIAnimationManager2::SetCompressPriorityComparison</a>  returns <b>S_OK</b> for all scheduled storyboards that might be affected by the compression. When the storyboards are compressed, time is temporarily accelerated for affected storyboards, so they play faster.</li>
</ul>


If none of the  preceding options is allowed by the priority comparison objects, the attempt to schedule the storyboard fails and Windows Animation returns <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_scheduling_result">UI_ANIMATION_SCHEDULING_INSUFFICIENT_PRIORITY</a> to the calling application.

Note that for the new storyboard to be successfully scheduled, it must begin before its longest acceptable delay has elapsed.  This is determined by <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay">IUIAnimationStoryboard::SetLongestAcceptableDelay</a> or <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setdefaultlongestacceptabledelay">IUIAnimationManager2::SetDefaultLongestAcceptableDelay</a> (if neither is called, the default is 0.0 seconds).  If the longest acceptable delay is <b>UI_ANIMATION_SECONDS_EVENTUALLY</b>, any finite delay will be sufficient.

The <i>priorityEffect</i> parameter describes the possible effect on the new storyboard if <b>HasPriority</b> were to return <b>S_FALSE</b>.  If <i>priorityEffect</i> is <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_priority_effect">UI_ANIMATION_PRIORITY_EFFECT_FAILURE</a>, it is possible that returning <b>S_FALSE</b> will result in a failure to schedule the new storyboard. (It is also possible that the animation manager will be allowed to resolve the conflict in a different way by another priority comparison object.)  If <i>priorityEffect</i> is <b>UI_ANIMATION_PRIORITY_EFFECT_DELAY</b>, the only downside of returning <b>S_FALSE</b> is that the storyboard might begin later than it would have if <i>HasPriority</i> had returned <b>S_OK</b>.

When <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_priority_effect">UI_ANIMATION_PRIORITY_EFFECT_DELAY</a> is passed to <b>HasPriority</b>, the animation manager has already determined that it can schedule the new storyboard to begin before its longest acceptable delay has elapsed, but it is in effect asking the application if the storyboard should begin even earlier.  In some scenarios, it might be best to reduce the latency of an animation by returning <b>S_OK</b>.  In others, it might be preferable to let scheduled animations complete whenever possible, in which case <b>HasPriority</b> should return <b>S_FALSE</b>.  <b>UI_ANIMATION_PRIORITY_EFFECT_DELAY</b> is only passed to <b>HasPriority</b> when the animation manager is considering canceling or trimming a storyboard.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setcancelprioritycomparison">IUIAnimationManager2::SetCancelPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setcompressprioritycomparison">IUIAnimationManager2::SetCompressPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setconcludeprioritycomparison">IUIAnimationManager2::SetConcludePriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-settrimprioritycomparison">IUIAnimationManager2::SetTrimPriorityComparison</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationprioritycomparison2">IUIAnimationPriorityComparison2</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_priority_effect">UI_ANIMATION_PRIORITY_EFFECT</a>