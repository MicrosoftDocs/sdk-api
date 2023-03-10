---
UID: NE:uianimation.__MIDL___MIDL_itf_UIAnimation_0000_0012_0001
title: UI_ANIMATION_IDLE_BEHAVIOR (uianimation.h)
description: Defines the behavior of a timer when the animation manager is idle.
helpviewer_keywords: ["UI_ANIMATION_IDLE_BEHAVIOR","UI_ANIMATION_IDLE_BEHAVIOR enumeration [Windows Animation]","UI_ANIMATION_IDLE_BEHAVIOR_CONTINUE","UI_ANIMATION_IDLE_BEHAVIOR_DISABLE","uianimation.ui_animation_idle_behavior","uianimation/UI_ANIMATION_IDLE_BEHAVIOR","uianimation/UI_ANIMATION_IDLE_BEHAVIOR_CONTINUE","uianimation/UI_ANIMATION_IDLE_BEHAVIOR_DISABLE"]
old-location: uianimation\ui_animation_idle_behavior.htm
tech.root: UIAnimation
ms.assetid: 70016fbd-060c-4f2a-89d3-d474850f9d01
ms.date: 12/05/2018
ms.keywords: UI_ANIMATION_IDLE_BEHAVIOR, UI_ANIMATION_IDLE_BEHAVIOR enumeration [Windows Animation], UI_ANIMATION_IDLE_BEHAVIOR_CONTINUE, UI_ANIMATION_IDLE_BEHAVIOR_DISABLE, uianimation.ui_animation_idle_behavior, uianimation/UI_ANIMATION_IDLE_BEHAVIOR, uianimation/UI_ANIMATION_IDLE_BEHAVIOR_CONTINUE, uianimation/UI_ANIMATION_IDLE_BEHAVIOR_DISABLE
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
req.typenames: UI_ANIMATION_IDLE_BEHAVIOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_UIAnimation_0000_0012_0001
 - uianimation/__MIDL___MIDL_itf_UIAnimation_0000_0012_0001
 - UI_ANIMATION_IDLE_BEHAVIOR
 - uianimation/UI_ANIMATION_IDLE_BEHAVIOR
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
 - UI_ANIMATION_IDLE_BEHAVIOR
---

# UI_ANIMATION_IDLE_BEHAVIOR enumeration


## -description

Defines the behavior of a timer when the animation manager is idle.

## -enum-fields

### -field UI_ANIMATION_IDLE_BEHAVIOR_CONTINUE:0

The timer continues to generate timer events (is enabled) when the animation manager is idle.

### -field UI_ANIMATION_IDLE_BEHAVIOR_DISABLE:1

The timer is suspended (disabled) when the animation manager is idle.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtimer">IUIAnimationTimer</a>
