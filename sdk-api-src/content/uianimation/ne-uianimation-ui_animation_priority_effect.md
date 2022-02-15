---
UID: NE:uianimation.__MIDL___MIDL_itf_UIAnimation_0000_0008_0001
title: UI_ANIMATION_PRIORITY_EFFECT (uianimation.h)
description: Defines potential effects on a storyboard if a priority comparison returns false.
helpviewer_keywords: ["UI_ANIMATION_PRIORITY_EFFECT","UI_ANIMATION_PRIORITY_EFFECT enumeration [Windows Animation]","UI_ANIMATION_PRIORITY_EFFECT_DELAY","UI_ANIMATION_PRIORITY_EFFECT_FAILURE","uianimation.ui_animation_priority_effect","uianimation/UI_ANIMATION_PRIORITY_EFFECT","uianimation/UI_ANIMATION_PRIORITY_EFFECT_DELAY","uianimation/UI_ANIMATION_PRIORITY_EFFECT_FAILURE"]
old-location: uianimation\ui_animation_priority_effect.htm
tech.root: UIAnimation
ms.assetid: 2da8fa3b-0947-46cb-bdb1-725da08b9aaa
ms.date: 12/05/2018
ms.keywords: UI_ANIMATION_PRIORITY_EFFECT, UI_ANIMATION_PRIORITY_EFFECT enumeration [Windows Animation], UI_ANIMATION_PRIORITY_EFFECT_DELAY, UI_ANIMATION_PRIORITY_EFFECT_FAILURE, uianimation.ui_animation_priority_effect, uianimation/UI_ANIMATION_PRIORITY_EFFECT, uianimation/UI_ANIMATION_PRIORITY_EFFECT_DELAY, uianimation/UI_ANIMATION_PRIORITY_EFFECT_FAILURE
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
req.typenames: UI_ANIMATION_PRIORITY_EFFECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_UIAnimation_0000_0008_0001
 - uianimation/__MIDL___MIDL_itf_UIAnimation_0000_0008_0001
 - UI_ANIMATION_PRIORITY_EFFECT
 - uianimation/UI_ANIMATION_PRIORITY_EFFECT
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
 - UI_ANIMATION_PRIORITY_EFFECT
---

# UI_ANIMATION_PRIORITY_EFFECT enumeration


## -description

Defines potential effects on a storyboard if a priority comparison returns false.

## -enum-fields

### -field UI_ANIMATION_PRIORITY_EFFECT_FAILURE:0

This storyboard might not be successfully scheduled.

### -field UI_ANIMATION_PRIORITY_EFFECT_DELAY:1

The storyboard will be scheduled, but might start playing later.

## -remarks

This enumeration is used as the <i>priorityEffect</i> parameter of  <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationprioritycomparison-haspriority">IUIAnimationPriorityComparison::HasPriority</a>, informing the client of the potential effect on the storyboard to be scheduled when the return value is false (S_FALSE).  UI_ANIMATION_PRIORITY_EFFECT_FAILURE means that the  attempt to schedule the storyboard might fail if the return value is false.   UI_ANIMATION_PRIORITY_EFFECT_DELAY means that the attempt to schedule the storyboard will succeed, but if the return value is false, the storyboard could play later than it would otherwise.

  This enumeration can help an application decide how aggressive to be about reducing latency in the UI. For example, if the application returns true when the effect is UI_ANIMATION_PRIORITY_EFFECT_DELAY, then other animations might get canceled or compressed even though doing so was not strictly necessary to play a new animation within the application-specified longest acceptable delay.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationprioritycomparison-haspriority">IUIAnimationPriorityComparison::HasPriority</a>
