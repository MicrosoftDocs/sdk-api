---
UID: NF:uianimation.IUIAnimationStoryboard.AddTransitionBetweenKeyframes
title: IUIAnimationStoryboard::AddTransitionBetweenKeyframes (uianimation.h)
description: Adds a transition between two keyframes. (IUIAnimationStoryboard.AddTransitionBetweenKeyframes)
helpviewer_keywords: ["AddTransitionBetweenKeyframes","AddTransitionBetweenKeyframes method [Windows Animation]","AddTransitionBetweenKeyframes method [Windows Animation]","IUIAnimationStoryboard interface","IUIAnimationStoryboard interface [Windows Animation]","AddTransitionBetweenKeyframes method","IUIAnimationStoryboard.AddTransitionBetweenKeyframes","IUIAnimationStoryboard::AddTransitionBetweenKeyframes","uianimation.iuianimationstoryboard_addtransitionbetweenkeyframes","uianimation/IUIAnimationStoryboard::AddTransitionBetweenKeyframes"]
old-location: uianimation\iuianimationstoryboard_addtransitionbetweenkeyframes.htm
tech.root: UIAnimation
ms.assetid: 75db41ef-526b-40aa-a62d-a4262cc8d80e
ms.date: 12/05/2018
ms.keywords: AddTransitionBetweenKeyframes, AddTransitionBetweenKeyframes method [Windows Animation], AddTransitionBetweenKeyframes method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],AddTransitionBetweenKeyframes method, IUIAnimationStoryboard.AddTransitionBetweenKeyframes, IUIAnimationStoryboard::AddTransitionBetweenKeyframes, uianimation.iuianimationstoryboard_addtransitionbetweenkeyframes, uianimation/IUIAnimationStoryboard::AddTransitionBetweenKeyframes
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
 - IUIAnimationStoryboard::AddTransitionBetweenKeyframes
 - uianimation/IUIAnimationStoryboard::AddTransitionBetweenKeyframes
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
 - IUIAnimationStoryboard.AddTransitionBetweenKeyframes
---

# IUIAnimationStoryboard::AddTransitionBetweenKeyframes


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

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

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

## -remarks

This method applies the specified transition to the specified variable in the storyboard, with the transition starting and ending at the specified keyframes.  If the transition was created with a duration parameter specified, that duration is overwritten with the duration of time between the start and end keyframes. Otherwise, Windows Animation speeds up or slows down the transition as necessary.

A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.

Transitions must be added in the order in which they will be played. A transition may begin playing before the preceding transition in the storyboard has finished, in which case the initial value and velocity seen by the new transition will be determined by the state of the preceding one. It must not be possible for a transition to begin before the start of the preceding transition.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset">IUIAnimationStoryboard::AddKeyframeAtOffset</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransition">IUIAnimationStoryboard::AddTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>
