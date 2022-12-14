---
UID: NF:uianimation.IUIAnimationStoryboard2.AddTransitionAtKeyframe
title: IUIAnimationStoryboard2::AddTransitionAtKeyframe (uianimation.h)
description: Adds a transition that starts at the specified keyframe. (IUIAnimationStoryboard2.AddTransitionAtKeyframe)
helpviewer_keywords: ["AddTransitionAtKeyframe","AddTransitionAtKeyframe method [Windows Animation]","AddTransitionAtKeyframe method [Windows Animation]","IUIAnimationStoryboard2 interface","IUIAnimationStoryboard2 interface [Windows Animation]","AddTransitionAtKeyframe method","IUIAnimationStoryboard2.AddTransitionAtKeyframe","IUIAnimationStoryboard2::AddTransitionAtKeyframe","uianimation.iuianimationstoryboard2_addtransitionatkeyframe","uianimation/IUIAnimationStoryboard2::AddTransitionAtKeyframe"]
old-location: uianimation\iuianimationstoryboard2_addtransitionatkeyframe.htm
tech.root: UIAnimation
ms.assetid: F4DAB833-E857-4FD8-87E2-8F32AF460F90
ms.date: 12/05/2018
ms.keywords: AddTransitionAtKeyframe, AddTransitionAtKeyframe method [Windows Animation], AddTransitionAtKeyframe method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],AddTransitionAtKeyframe method, IUIAnimationStoryboard2.AddTransitionAtKeyframe, IUIAnimationStoryboard2::AddTransitionAtKeyframe, uianimation.iuianimationstoryboard2_addtransitionatkeyframe, uianimation/IUIAnimationStoryboard2::AddTransitionAtKeyframe
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
 - IUIAnimationStoryboard2::AddTransitionAtKeyframe
 - uianimation/IUIAnimationStoryboard2::AddTransitionAtKeyframe
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
 - IUIAnimationStoryboard2.AddTransitionAtKeyframe
---

# IUIAnimationStoryboard2::AddTransitionAtKeyframe


## -description

Adds a transition that starts at the specified keyframe.

## -parameters

### -param variable [in]

The animation variable for which a transition is to be added.

### -param transition [in]

The transition to be added.

### -param startKeyframe [in]

The keyframe that specifies the beginning of the new transition.

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
</table>
 

See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Transitions must be added in the order in which they will be played. A transition may begin playing before the preceding transition in the storyboard has finished, in which case the initial value and velocity seen by the new transition is determined by the state of the preceding one. A transition should not begin before the start of the preceding transition.

A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeaftertransition">IUIAnimationStoryboard2::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeatoffset">IUIAnimationStoryboard2::AddKeyframeAtOffset</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransition">IUIAnimationStoryboard2::AddTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionbetweenkeyframes">IUIAnimationStoryboard2::AddTransitionBetweenKeyframes</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>
