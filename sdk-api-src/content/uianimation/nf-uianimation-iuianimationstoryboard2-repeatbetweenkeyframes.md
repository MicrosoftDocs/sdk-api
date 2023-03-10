---
UID: NF:uianimation.IUIAnimationStoryboard2.RepeatBetweenKeyframes
title: IUIAnimationStoryboard2::RepeatBetweenKeyframes (uianimation.h)
description: Creates a loop between two keyframes.
helpviewer_keywords: ["IUIAnimationStoryboard2 interface [Windows Animation]","RepeatBetweenKeyframes method","IUIAnimationStoryboard2.RepeatBetweenKeyframes","IUIAnimationStoryboard2::RepeatBetweenKeyframes","RepeatBetweenKeyframes","RepeatBetweenKeyframes method [Windows Animation]","RepeatBetweenKeyframes method [Windows Animation]","IUIAnimationStoryboard2 interface","uianimation.iuianimationstoryboard2_repeatbetweenkeyframes","uianimation/IUIAnimationStoryboard2::RepeatBetweenKeyframes"]
old-location: uianimation\iuianimationstoryboard2_repeatbetweenkeyframes.htm
tech.root: UIAnimation
ms.assetid: 31BC2628-14B3-4405-BA9B-4FB275D9AC0D
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard2 interface [Windows Animation],RepeatBetweenKeyframes method, IUIAnimationStoryboard2.RepeatBetweenKeyframes, IUIAnimationStoryboard2::RepeatBetweenKeyframes, RepeatBetweenKeyframes, RepeatBetweenKeyframes method [Windows Animation], RepeatBetweenKeyframes method [Windows Animation],IUIAnimationStoryboard2 interface, uianimation.iuianimationstoryboard2_repeatbetweenkeyframes, uianimation/IUIAnimationStoryboard2::RepeatBetweenKeyframes
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
 - IUIAnimationStoryboard2::RepeatBetweenKeyframes
 - uianimation/IUIAnimationStoryboard2::RepeatBetweenKeyframes
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
 - IUIAnimationStoryboard2.RepeatBetweenKeyframes
---

# IUIAnimationStoryboard2::RepeatBetweenKeyframes


## -description

Creates a loop between two keyframes.

## -parameters

### -param startKeyframe [in]

The keyframe at which the loop is to begin.

### -param endKeyframe [in]

The keyframe at which the loop is to end. <i>endKeyframe</i> must not occur earlier in the storyboard than <i>startKeyframe</i>.

### -param cRepetition [in]

The number of times the loop is to be repeated; the last iteration of a loop can terminate fractionally between keyframes. A value of  zero indicates that the specified portion of a storyboard will not be played.  A value of <a href="/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a> (-1) indicates that the loop will repeat indefinitely until the storyboard is trimmed or concluded.

### -param repeatMode [in]

The pattern for the loop iteration. 

A value of <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_repeat_mode">UI_ANIMATION_REPEAT_MODE_ALTERNATE</a> (1) specifies that the  start of the loop must alternate between keyframes (k1-&gt;k2, k2-&gt;k1, k1-&gt;k2, and so on).

A value of <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_repeat_mode">UI_ANIMATION_REPEAT_MODE_NORMAL</a> (0) specifies that the start of the  loop must begin with the first keyframe (k1-&gt;k2, k1-&gt;k2, k1-&gt;k2, and so on).

<div class="alert"><b>Note</b>  If <i>repeatMode</i> has a value of <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_repeat_mode">UI_ANIMATION_REPEAT_MODE_ALTERNATE</a> (1) and <i>cRepetition</i> has a value of <a href="/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a> (-1), the loop terminates on the end keyframe.
</div>
<div> </div>

### -param pIterationChangeHandler [in]

The handler for each loop iteration event. The default value is 0.

### -param id [in]

The loop ID to pass to <i>pIterationChangeHandler</i>. The default value is 0.

### -param fRegisterForNextAnimationEvent [in]

If true, specifies that <i>pIterationChangeHandler</i> will be incorporated into the estimate of the time interval until the next animation event that is returned by the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-estimatenexteventtime">IUIAnimationManager2::EstimateNextEventTime</a> method. The default value is 0, or false.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method directs a storyboard to play the interval between the given keyframes repeatedly before playing the remainder of the storyboard. If a finite repetition count is specified, the loop always plays that number of times. If <a href="/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a> (-1) is specified, the loop repeats until the storyboard is concluded, in which case the current iteration of the loop completes and the remainder of the storyboard plays. A storyboard that loops indefinitely also ends if it is truncated.

Nested and overlapping loops are not supported.

A keyframe represents a moment in time within a storyboard and can be used to specify the start or end times of transitions.  Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeaftertransition">IUIAnimationStoryboard2::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeatoffset">IUIAnimationStoryboard2::AddKeyframeAtOffset</a>