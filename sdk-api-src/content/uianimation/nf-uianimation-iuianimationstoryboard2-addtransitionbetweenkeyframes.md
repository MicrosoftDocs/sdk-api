---
UID: NF:uianimation.IUIAnimationStoryboard2.AddTransitionBetweenKeyframes
title: IUIAnimationStoryboard2::AddTransitionBetweenKeyframes (uianimation.h)
description: Adds a transition between two keyframes. (IUIAnimationStoryboard2.AddTransitionBetweenKeyframes)
helpviewer_keywords: ["AddTransitionBetweenKeyframes","AddTransitionBetweenKeyframes method [Windows Animation]","AddTransitionBetweenKeyframes method [Windows Animation]","IUIAnimationStoryboard2 interface","IUIAnimationStoryboard2 interface [Windows Animation]","AddTransitionBetweenKeyframes method","IUIAnimationStoryboard2.AddTransitionBetweenKeyframes","IUIAnimationStoryboard2::AddTransitionBetweenKeyframes","uianimation.iuianimationstoryboard2_addtransitionbetweenkeyframes","uianimation/IUIAnimationStoryboard2::AddTransitionBetweenKeyframes"]
old-location: uianimation\iuianimationstoryboard2_addtransitionbetweenkeyframes.htm
tech.root: UIAnimation
ms.assetid: 55AEA5EA-7D9E-4669-8315-7A6F4428EDF9
ms.date: 12/05/2018
ms.keywords: AddTransitionBetweenKeyframes, AddTransitionBetweenKeyframes method [Windows Animation], AddTransitionBetweenKeyframes method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],AddTransitionBetweenKeyframes method, IUIAnimationStoryboard2.AddTransitionBetweenKeyframes, IUIAnimationStoryboard2::AddTransitionBetweenKeyframes, uianimation.iuianimationstoryboard2_addtransitionbetweenkeyframes, uianimation/IUIAnimationStoryboard2::AddTransitionBetweenKeyframes
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
 - IUIAnimationStoryboard2::AddTransitionBetweenKeyframes
 - uianimation/IUIAnimationStoryboard2::AddTransitionBetweenKeyframes
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
 - IUIAnimationStoryboard2.AddTransitionBetweenKeyframes
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
 

See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method applies the specified transition to the specified variable in the storyboard, with the transition starting and ending at the specified keyframes.  If the transition was created with a duration parameter specified, that duration is overwritten with the duration of time between the start and end keyframes. Otherwise, Windows Animation speeds up or slows down the transition as necessary.

A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.

Transitions must be added in the order in which they will be played. A transition may begin playing before the preceding transition in the storyboard has finished, in which case the initial value and velocity seen by the new transition will be determined by the state of the preceding one. It must not be possible for a transition to begin before the start of the preceding transition.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeaftertransition">IUIAnimationStoryboard2::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeatoffset">IUIAnimationStoryboard2::AddKeyframeAtOffset</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransition">IUIAnimationStoryboard2::AddTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionatkeyframe">IUIAnimationStoryboard2::AddTransitionAtKeyframe</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>
