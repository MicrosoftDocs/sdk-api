---
UID: NF:uianimation.IUIAnimationManager.SetAnimationMode
title: IUIAnimationManager::SetAnimationMode (uianimation.h)
description: Sets the animation mode. (IUIAnimationManager.SetAnimationMode)
helpviewer_keywords: ["IUIAnimationManager interface [Windows Animation]","SetAnimationMode method","IUIAnimationManager.SetAnimationMode","IUIAnimationManager::SetAnimationMode","SetAnimationMode","SetAnimationMode method [Windows Animation]","SetAnimationMode method [Windows Animation]","IUIAnimationManager interface","uianimation.iuianimationmanager_setanimationmode","uianimation/IUIAnimationManager::SetAnimationMode"]
old-location: uianimation\iuianimationmanager_setanimationmode.htm
tech.root: UIAnimation
ms.assetid: b5d6c5f1-1e1c-497f-a556-f419e2c68585
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],SetAnimationMode method, IUIAnimationManager.SetAnimationMode, IUIAnimationManager::SetAnimationMode, SetAnimationMode, SetAnimationMode method [Windows Animation], SetAnimationMode method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_setanimationmode, uianimation/IUIAnimationManager::SetAnimationMode
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
 - IUIAnimationManager::SetAnimationMode
 - uianimation/IUIAnimationManager::SetAnimationMode
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
 - IUIAnimationManager.SetAnimationMode
---

# IUIAnimationManager::SetAnimationMode


## -description

Sets the animation mode.

## -parameters

### -param mode [in]

The animation mode.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method is used to enable or disable animation globally. While animation is disabled, all storyboards finish immediately when they are scheduled. The default mode is <b>UI_ANIMATION_MODE_SYSTEM_DEFAULT</b>, which lets Windows decide when to enable or disable animation in the application.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_mode">UI_ANIMATION_MODE</a>
