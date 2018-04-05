---
UID: NE:uianimation.__MIDL___MIDL_itf_UIAnimation_0000_0012_0001
title: "__MIDL___MIDL_itf_UIAnimation_0000_0012_0001"
author: windows-driver-content
description: Defines the behavior of a timer when the animation manager is idle.
old-location: uianimation\ui_animation_idle_behavior.htm
old-project: UIAnimation
ms.assetid: 70016fbd-060c-4f2a-89d3-d474850f9d01
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: UI_ANIMATION_IDLE_BEHAVIOR, UI_ANIMATION_IDLE_BEHAVIOR enumeration [Windows Animation], UI_ANIMATION_IDLE_BEHAVIOR_CONTINUE, UI_ANIMATION_IDLE_BEHAVIOR_DISABLE, __MIDL___MIDL_itf_UIAnimation_0000_0012_0001, uianimation.ui_animation_idle_behavior, uianimation/UI_ANIMATION_IDLE_BEHAVIOR, uianimation/UI_ANIMATION_IDLE_BEHAVIOR_CONTINUE, uianimation/UI_ANIMATION_IDLE_BEHAVIOR_DISABLE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps | UWP apps]
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
req.typenames: UI_ANIMATION_IDLE_BEHAVIOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	UIAnimation.h
api_name:
-	UI_ANIMATION_IDLE_BEHAVIOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# __MIDL___MIDL_itf_UIAnimation_0000_0012_0001 enumeration


## -description



         Defines the behavior of a timer when the animation manager is idle.


## -enum-fields




### -field UI_ANIMATION_IDLE_BEHAVIOR_CONTINUE


            The timer continues to generate timer events (is enabled) when the animation manager is idle.


### -field UI_ANIMATION_IDLE_BEHAVIOR_DISABLE


            The timer is suspended (disabled) when the animation manager is idle.
         


## -see-also




<a href="https://msdn.microsoft.com/75d29528-005e-4f49-b8ff-651b58d58fc7">IUIAnimationTimer</a>
 

 

