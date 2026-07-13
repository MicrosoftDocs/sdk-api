---
UID: NF:uianimation.IUIAnimationStoryboard2.AddKeyframeAfterTransition
title: IUIAnimationStoryboard2::AddKeyframeAfterTransition (uianimation.h)
description: Adds a keyframe at the end of the specified transition. (IUIAnimationStoryboard2.AddKeyframeAfterTransition)
helpviewer_keywords: ["AddKeyframeAfterTransition","AddKeyframeAfterTransition method [Windows Animation]","AddKeyframeAfterTransition method [Windows Animation]","IUIAnimationStoryboard2 interface","IUIAnimationStoryboard2 interface [Windows Animation]","AddKeyframeAfterTransition method","IUIAnimationStoryboard2.AddKeyframeAfterTransition","IUIAnimationStoryboard2::AddKeyframeAfterTransition","uianimation.iuianimationstoryboard2_addkeyframeaftertransition","uianimation/IUIAnimationStoryboard2::AddKeyframeAfterTransition"]
old-location: uianimation\iuianimationstoryboard2_addkeyframeaftertransition.htm
tech.root: UIAnimation
ms.assetid: F5D13D36-1AEE-4D47-9683-A428E9ADF1D6
ms.date: 12/05/2018
ms.keywords: AddKeyframeAfterTransition, AddKeyframeAfterTransition method [Windows Animation], AddKeyframeAfterTransition method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],AddKeyframeAfterTransition method, IUIAnimationStoryboard2.AddKeyframeAfterTransition, IUIAnimationStoryboard2::AddKeyframeAfterTransition, uianimation.iuianimationstoryboard2_addkeyframeaftertransition, uianimation/IUIAnimationStoryboard2::AddKeyframeAfterTransition
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
 - IUIAnimationStoryboard2::AddKeyframeAfterTransition
 - uianimation/IUIAnimationStoryboard2::AddKeyframeAfterTransition
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
 - IUIAnimationStoryboard2.AddKeyframeAfterTransition
---

# IUIAnimationStoryboard2::AddKeyframeAfterTransition


## -description

Adds a keyframe at the end of the specified transition.

## -parameters

### -param transition [in]

The transition after which a keyframe is to be added.

### -param keyframe [out]

The keyframe to be added.

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
<dt><b>UI_E_TRANSITION_NOT_IN_STORYBOARD</b></dt>
</dl>
</td>
<td width="60%">
The transition has not been added to the storyboard.

</td>
</tr>
</table>
 

See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeatoffset">IUIAnimationStoryboard2::AddKeyframeAtOffset</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransition">IUIAnimationStoryboard2::AddTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionatkeyframe">IUIAnimationStoryboard2::AddTransitionAtKeyframe</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionbetweenkeyframes">IUIAnimationStoryboard2::AddTransitionBetweenKeyframes</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransitionlibrary2">IUIAnimationTransitionLibrary2</a>



<a href="/windows/win32/api/uianimation/ns-uianimation-__midl___midl_itf_uianimation_0000_0002_0003">UI_ANIMATION_KEYFRAME</a>
