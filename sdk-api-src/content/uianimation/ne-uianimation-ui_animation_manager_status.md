---
UID: NE:uianimation.__MIDL___MIDL_itf_UIAnimation_0000_0000_0002
title: UI_ANIMATION_MANAGER_STATUS (uianimation.h)
description: Defines the activity status of an animation manager.
helpviewer_keywords: ["UI_ANIMATION_MANAGER_BUSY","UI_ANIMATION_MANAGER_IDLE","UI_ANIMATION_MANAGER_STATUS","UI_ANIMATION_MANAGER_STATUS enumeration [Windows Animation]","uianimation.ui_animation_manager_status","uianimation/UI_ANIMATION_MANAGER_BUSY","uianimation/UI_ANIMATION_MANAGER_IDLE","uianimation/UI_ANIMATION_MANAGER_STATUS"]
old-location: uianimation\ui_animation_manager_status.htm
tech.root: UIAnimation
ms.assetid: 499c74c0-d1e7-4ab4-9c3a-19c2e1abeda8
ms.date: 12/05/2018
ms.keywords: UI_ANIMATION_MANAGER_BUSY, UI_ANIMATION_MANAGER_IDLE, UI_ANIMATION_MANAGER_STATUS, UI_ANIMATION_MANAGER_STATUS enumeration [Windows Animation], uianimation.ui_animation_manager_status, uianimation/UI_ANIMATION_MANAGER_BUSY, uianimation/UI_ANIMATION_MANAGER_IDLE, uianimation/UI_ANIMATION_MANAGER_STATUS
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
req.typenames: UI_ANIMATION_MANAGER_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_UIAnimation_0000_0000_0002
 - uianimation/__MIDL___MIDL_itf_UIAnimation_0000_0000_0002
 - UI_ANIMATION_MANAGER_STATUS
 - uianimation/UI_ANIMATION_MANAGER_STATUS
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
 - UI_ANIMATION_MANAGER_STATUS
---

# UI_ANIMATION_MANAGER_STATUS enumeration


## -description

Defines the activity status of an animation manager.

## -enum-fields

### -field UI_ANIMATION_MANAGER_IDLE:0

The animation manager is idle; no animations are currently playing.

### -field UI_ANIMATION_MANAGER_BUSY:1

The animation manager is busy; at least one animation is currently playing or scheduled.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstatus">IUIAnimationManager::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanagereventhandler-onmanagerstatuschanged">IUIAnimationManagerEventHandler::OnManagerStatusChanged</a>
