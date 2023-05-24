---
UID: NF:uianimation.IUIAnimationStoryboard2.AddKeyframeAtOffset
title: IUIAnimationStoryboard2::AddKeyframeAtOffset (uianimation.h)
description: Adds a keyframe at the specified offset from an existing keyframe. (IUIAnimationStoryboard2.AddKeyframeAtOffset)
helpviewer_keywords: ["AddKeyframeAtOffset","AddKeyframeAtOffset method [Windows Animation]","AddKeyframeAtOffset method [Windows Animation]","IUIAnimationStoryboard2 interface","IUIAnimationStoryboard2 interface [Windows Animation]","AddKeyframeAtOffset method","IUIAnimationStoryboard2.AddKeyframeAtOffset","IUIAnimationStoryboard2::AddKeyframeAtOffset","uianimation.iuianimationstoryboard2_addkeyframeatoffset","uianimation/IUIAnimationStoryboard2::AddKeyframeAtOffset"]
old-location: uianimation\iuianimationstoryboard2_addkeyframeatoffset.htm
tech.root: UIAnimation
ms.assetid: 6AB47BC1-4437-4191-8B66-8545EB4102A9
ms.date: 12/05/2018
ms.keywords: AddKeyframeAtOffset, AddKeyframeAtOffset method [Windows Animation], AddKeyframeAtOffset method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],AddKeyframeAtOffset method, IUIAnimationStoryboard2.AddKeyframeAtOffset, IUIAnimationStoryboard2::AddKeyframeAtOffset, uianimation.iuianimationstoryboard2_addkeyframeatoffset, uianimation/IUIAnimationStoryboard2::AddKeyframeAtOffset
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
 - IUIAnimationStoryboard2::AddKeyframeAtOffset
 - uianimation/IUIAnimationStoryboard2::AddKeyframeAtOffset
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
 - IUIAnimationStoryboard2.AddKeyframeAtOffset
---

# IUIAnimationStoryboard2::AddKeyframeAtOffset


## -description

Adds a keyframe at the specified offset from an existing keyframe.

## -parameters

### -param existingKeyframe [in]

The existing keyframe. To add a keyframe at an offset from the start of the storyboard, use the special keyframe <a href="/previous-versions/windows/desktop/legacy/dd756780(v=vs.85)">UI_ANIMATION_KEYFRAME_STORYBOARD_START</a>.

### -param offset [in]

The offset from the existing keyframe at which a new keyframe is to be added.

### -param keyframe [out]

The keyframe to be added.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addkeyframeaftertransition">IUIAnimationStoryboard2::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionatkeyframe">IUIAnimationStoryboard2::AddTransitionAtKeyframe</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-addtransitionbetweenkeyframes">IUIAnimationStoryboard2::AddTransitionBetweenKeyframes</a>



<a href="/windows/win32/api/uianimation/ns-uianimation-__midl___midl_itf_uianimation_0000_0002_0003">UI_ANIMATION_KEYFRAME</a>
