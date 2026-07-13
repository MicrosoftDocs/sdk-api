---
UID: NF:uianimation.IUIAnimationStoryboard.AddKeyframeAfterTransition
title: IUIAnimationStoryboard::AddKeyframeAfterTransition (uianimation.h)
description: Adds a keyframe at the end of the specified transition. (IUIAnimationStoryboard.AddKeyframeAfterTransition)
helpviewer_keywords: ["AddKeyframeAfterTransition","AddKeyframeAfterTransition method [Windows Animation]","AddKeyframeAfterTransition method [Windows Animation]","IUIAnimationStoryboard interface","IUIAnimationStoryboard interface [Windows Animation]","AddKeyframeAfterTransition method","IUIAnimationStoryboard.AddKeyframeAfterTransition","IUIAnimationStoryboard::AddKeyframeAfterTransition","uianimation.iuianimationstoryboard_addkeyframeaftertransition","uianimation/IUIAnimationStoryboard::AddKeyframeAfterTransition"]
old-location: uianimation\iuianimationstoryboard_addkeyframeaftertransition.htm
tech.root: UIAnimation
ms.assetid: 055206d8-ea9e-4013-89ee-2929bfeb2731
ms.date: 12/05/2018
ms.keywords: AddKeyframeAfterTransition, AddKeyframeAfterTransition method [Windows Animation], AddKeyframeAfterTransition method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],AddKeyframeAfterTransition method, IUIAnimationStoryboard.AddKeyframeAfterTransition, IUIAnimationStoryboard::AddKeyframeAfterTransition, uianimation.iuianimationstoryboard_addkeyframeaftertransition, uianimation/IUIAnimationStoryboard::AddKeyframeAfterTransition
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
 - IUIAnimationStoryboard::AddKeyframeAfterTransition
 - uianimation/IUIAnimationStoryboard::AddKeyframeAfterTransition
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
 - IUIAnimationStoryboard.AddKeyframeAfterTransition
---

# IUIAnimationStoryboard::AddKeyframeAfterTransition


## -description

Adds a keyframe at the end of the specified transition.

## -parameters

### -param transition [in]

The transition after which a keyframe is to be added.

### -param keyframe [out]

The keyframe to be added.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes"> Windows Animation Error Codes</a> for a list of error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UI_E_TRANSITION_NOT_IN_STORYBOARD</b></dt>
</dl>
</td>
<td width="60%">
The transition has not been added to the storyboard.

</td>
</tr>
</table>

## -remarks

A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset">IUIAnimationStoryboard::AddKeyframeAtOffset</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransition">IUIAnimationStoryboard::AddTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary">IUIAnimationTransitionLibrary</a>



<a href="/windows/win32/api/uianimation/ns-uianimation-__midl___midl_itf_uianimation_0000_0002_0003">UI_ANIMATION_KEYFRAME</a>
