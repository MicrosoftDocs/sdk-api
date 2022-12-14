---
UID: NF:uianimation.IUIAnimationStoryboard.RepeatBetweenKeyframes
title: IUIAnimationStoryboard::RepeatBetweenKeyframes (uianimation.h)
description: Creates a loop between two specified keyframes.
helpviewer_keywords: ["IUIAnimationStoryboard interface [Windows Animation]","RepeatBetweenKeyframes method","IUIAnimationStoryboard.RepeatBetweenKeyframes","IUIAnimationStoryboard::RepeatBetweenKeyframes","RepeatBetweenKeyframes","RepeatBetweenKeyframes method [Windows Animation]","RepeatBetweenKeyframes method [Windows Animation]","IUIAnimationStoryboard interface","uianimation.iuianimationstoryboard_repeatbetweenkeyframes","uianimation/IUIAnimationStoryboard::RepeatBetweenKeyframes"]
old-location: uianimation\iuianimationstoryboard_repeatbetweenkeyframes.htm
tech.root: UIAnimation
ms.assetid: 3c1ddb8c-fcbf-4b0c-8725-35dfc15e3c02
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard interface [Windows Animation],RepeatBetweenKeyframes method, IUIAnimationStoryboard.RepeatBetweenKeyframes, IUIAnimationStoryboard::RepeatBetweenKeyframes, RepeatBetweenKeyframes, RepeatBetweenKeyframes method [Windows Animation], RepeatBetweenKeyframes method [Windows Animation],IUIAnimationStoryboard interface, uianimation.iuianimationstoryboard_repeatbetweenkeyframes, uianimation/IUIAnimationStoryboard::RepeatBetweenKeyframes
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
 - IUIAnimationStoryboard::RepeatBetweenKeyframes
 - uianimation/IUIAnimationStoryboard::RepeatBetweenKeyframes
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
 - IUIAnimationStoryboard.RepeatBetweenKeyframes
---

# IUIAnimationStoryboard::RepeatBetweenKeyframes


## -description

Creates a loop between two specified keyframes.

## -parameters

### -param startKeyframe [in]

The keyframe at which the loop is to begin.

### -param endKeyframe [in]

The keyframe at which the loop is to end. It must not be possible for <i>endKeyframe</i> to occur earlier in the storyboard than <i>startKeyframe</i>.

### -param repetitionCount [in]

The number of times the loop is to be repeated; this parameter must be 0 or a positive number.
               Use <a href="/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a> (-1) to repeat the loop indefinitely until the storyboard is trimmed or concluded.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_END_KEYFRAME_NOT_DETERMINED</b></dt>
</dl>
</td>
<td width="60%">
It might not be possible to determine the end keyframe time when the start keyframe is reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_LOOPS_OVERLAP</b></dt>
</dl>
</td>
<td width="60%">
Two repeated portions of a storyboard might overlap.

</td>
</tr>
</table>

## -remarks

This method directs a storyboard to play the interval between the given keyframes repeatedly before playing the remainder of the storyboard. If a finite repetition count is specified, the loop always plays that number of times. If <a href="/windows/desktop/UIAnimation/ui-animation-repeat-indefinitely">UI_ANIMATION_REPEAT_INDEFINITELY</a> (-1) is specified, the loop repeats until the storyboard is concluded, in which case the current iteration of the loop completes and the remainder of the storyboard plays. A storyboard that loops indefinitely also ends if it is truncated.

Nested and overlapping loops are not supported.

A keyframe represents a moment in time within a storyboard and can be used to specify the start or end times of transitions.  Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset">IUIAnimationStoryboard::AddKeyframeAtOffset</a>