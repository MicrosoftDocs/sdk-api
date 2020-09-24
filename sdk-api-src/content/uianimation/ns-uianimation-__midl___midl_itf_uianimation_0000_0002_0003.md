---
UID: NS:uianimation.__MIDL___MIDL_itf_UIAnimation_0000_0002_0003
title: __MIDL___MIDL_itf_UIAnimation_0000_0002_0003 (uianimation.h)
description: Defines a keyframe, which represents a time offset within a storyboard.
helpviewer_keywords: ["*UI_ANIMATION_KEYFRAME","UI_ANIMATION_KEYFRAME","UI_ANIMATION_KEYFRAME structure [Windows Animation]","__MIDL___MIDL_itf_UIAnimation_0000_0002_0003","uianimation.ui_animation_keyframe","uianimation/UI_ANIMATION_KEYFRAME"]
old-location: uianimation\ui_animation_keyframe.htm
tech.root: UIAnimation
ms.assetid: 4ac3d524-35a6-4cb9-a468-b7f88500a49c
ms.date: 12/05/2018
ms.keywords: '*UI_ANIMATION_KEYFRAME, UI_ANIMATION_KEYFRAME, UI_ANIMATION_KEYFRAME structure [Windows Animation], __MIDL___MIDL_itf_UIAnimation_0000_0002_0003, uianimation.ui_animation_keyframe, uianimation/UI_ANIMATION_KEYFRAME'
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: '*UI_ANIMATION_KEYFRAME'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_UIAnimation_0000_0002_0003
 - uianimation/__MIDL___MIDL_itf_UIAnimation_0000_0002_0003
 - UI_ANIMATION_KEYFRAME
 - uianimation/UI_ANIMATION_KEYFRAME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAnimation.h
api_name:
 - UI_ANIMATION_KEYFRAME
---

# __MIDL___MIDL_itf_UIAnimation_0000_0002_0003 structure


## -description

Defines a keyframe, which represents a time offset within a storyboard.

## -struct-fields

## -remarks

This structure should be treated as a handle. It is returned as an output parameter by some methods and should be used only as a  parameter passed back to other methods as an input parameter.


<a href="/previous-versions/windows/desktop/legacy/dd756780(v=vs.85)">UI_ANIMATION_KEYFRAME_STORYBOARD_START</a> represents the implicit keyframe at the start of every storyboard.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition">IUIAnimationStoryboard::AddKeyframeAfterTransition</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset">IUIAnimationStoryboard::AddKeyframeAtOffset</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionatkeyframe">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-repeatbetweenkeyframes">IUIAnimationStoryboard::RepeatBetweenKeyframes</a>