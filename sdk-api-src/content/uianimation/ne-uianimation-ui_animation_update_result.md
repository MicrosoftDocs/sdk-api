---
UID: NE:uianimation.__MIDL___MIDL_itf_UIAnimation_0000_0000_0001
title: UI_ANIMATION_UPDATE_RESULT (uianimation.h)
description: Defines results for animation updates.
helpviewer_keywords: ["UI_ANIMATION_UPDATE_NO_CHANGE","UI_ANIMATION_UPDATE_RESULT","UI_ANIMATION_UPDATE_RESULT enumeration [Windows Animation]","UI_ANIMATION_UPDATE_VARIABLES_CHANGED","uianimation.ui_animation_update_result","uianimation/UI_ANIMATION_UPDATE_NO_CHANGE","uianimation/UI_ANIMATION_UPDATE_RESULT","uianimation/UI_ANIMATION_UPDATE_VARIABLES_CHANGED"]
old-location: uianimation\ui_animation_update_result.htm
tech.root: UIAnimation
ms.assetid: 19b1d80f-39b3-4046-aa6a-5312e004b4b0
ms.date: 12/05/2018
ms.keywords: UI_ANIMATION_UPDATE_NO_CHANGE, UI_ANIMATION_UPDATE_RESULT, UI_ANIMATION_UPDATE_RESULT enumeration [Windows Animation], UI_ANIMATION_UPDATE_VARIABLES_CHANGED, uianimation.ui_animation_update_result, uianimation/UI_ANIMATION_UPDATE_NO_CHANGE, uianimation/UI_ANIMATION_UPDATE_RESULT, uianimation/UI_ANIMATION_UPDATE_VARIABLES_CHANGED
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
req.typenames: UI_ANIMATION_UPDATE_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_UIAnimation_0000_0000_0001
 - uianimation/__MIDL___MIDL_itf_UIAnimation_0000_0000_0001
 - UI_ANIMATION_UPDATE_RESULT
 - uianimation/UI_ANIMATION_UPDATE_RESULT
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
 - UI_ANIMATION_UPDATE_RESULT
---

# UI_ANIMATION_UPDATE_RESULT enumeration


## -description

Defines results for animation updates.

## -enum-fields

### -field UI_ANIMATION_UPDATE_NO_CHANGE:0

No animation variables have changed.

### -field UI_ANIMATION_UPDATE_VARIABLES_CHANGED:1

One or more animation variables has changed.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-update">IUIAnimationManager::Update</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtimerupdatehandler-onupdate">IUIAnimationTimerUpdateHandler::OnUpdate</a>
