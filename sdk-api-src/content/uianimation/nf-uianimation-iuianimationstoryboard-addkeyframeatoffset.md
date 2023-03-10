---
UID: NF:uianimation.IUIAnimationStoryboard.AddKeyframeAtOffset
title: IUIAnimationStoryboard::AddKeyframeAtOffset (uianimation.h)
description: Adds a keyframe at the specified offset from an existing keyframe. (IUIAnimationStoryboard.AddKeyframeAtOffset)
helpviewer_keywords: ["AddKeyframeAtOffset","AddKeyframeAtOffset method [Windows Animation]","AddKeyframeAtOffset method [Windows Animation]","IUIAnimationStoryboard interface","IUIAnimationStoryboard interface [Windows Animation]","AddKeyframeAtOffset method","IUIAnimationStoryboard.AddKeyframeAtOffset","IUIAnimationStoryboard::AddKeyframeAtOffset","uianimation.iuianimationstoryboard_addkeyframeatoffset","uianimation/IUIAnimationStoryboard::AddKeyframeAtOffset"]
old-location: uianimation\iuianimationstoryboard_addkeyframeatoffset.htm
tech.root: UIAnimation
ms.assetid: f598c8a4-4325-49ed-bc18-5d672e089592
ms.date: 12/05/2018
ms.keywords: AddKeyframeAtOffset, AddKeyframeAtOffset method [Windows Animation], AddKeyframeAtOffset method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],AddKeyframeAtOffset method, IUIAnimationStoryboard.AddKeyframeAtOffset, IUIAnimationStoryboard::AddKeyframeAtOffset, uianimation.iuianimationstoryboard_addkeyframeatoffset, uianimation/IUIAnimationStoryboard::AddKeyframeAtOffset
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
 - IUIAnimationStoryboard::AddKeyframeAtOffset
 - uianimation/IUIAnimationStoryboard::AddKeyframeAtOffset
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
 - IUIAnimationStoryboard.AddKeyframeAtOffset
---

# IUIAnimationStoryboard::AddKeyframeAtOffset


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

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A keyframe represents a moment in time within a storyboard and can be used to specify the start and end times of transitions. Because keyframes can be added at the ends of transitions, their offsets from the start of the storyboard may not be known until the storyboard is playing.


#### Examples

The following code adds a keyframe at a fixed offset of 0.3 seconds from the keyframe at the start of the storyboard.


```cpp
const UI_ANIMATION_SECONDS offset = 0.3;

UI_ANIMATION_KEYFRAME keyframe1;
hr = pStoryboard->AddKeyframeAtOffset(
       UI_ANIMATION_KEYFRAME_STORYBOARD_START,
       offset,
       &keyframe1
);
```

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="/windows/win32/api/uianimation/ns-uianimation-__midl___midl_itf_uianimation_0000_0002_0003">UI_ANIMATION_KEYFRAME</a>
