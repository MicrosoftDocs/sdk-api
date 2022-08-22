---
UID: NF:uianimation.IUIAnimationManager.Pause
title: IUIAnimationManager::Pause (uianimation.h)
description: Pauses all animations. (IUIAnimationManager.Pause)
helpviewer_keywords: ["IUIAnimationManager interface [Windows Animation]","Pause method","IUIAnimationManager.Pause","IUIAnimationManager::Pause","Pause","Pause method [Windows Animation]","Pause method [Windows Animation]","IUIAnimationManager interface","uianimation.iuianimationmanager_pause","uianimation/IUIAnimationManager::Pause"]
old-location: uianimation\iuianimationmanager_pause.htm
tech.root: UIAnimation
ms.assetid: 52b11e79-9930-4fd8-84b4-152917090519
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],Pause method, IUIAnimationManager.Pause, IUIAnimationManager::Pause, Pause, Pause method [Windows Animation], Pause method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_pause, uianimation/IUIAnimationManager::Pause
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
 - IUIAnimationManager::Pause
 - uianimation/IUIAnimationManager::Pause
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
 - IUIAnimationManager.Pause
---

# IUIAnimationManager::Pause


## -description

Pauses all animations.



## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

When an animation manager is paused, its status is set to <b>UI_ANIMATION_MANAGER_IDLE</b>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstatus">IUIAnimationManager::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-resume">IUIAnimationManager::Resume</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_manager_status">UI_ANIMATION_MANAGER_STATUS</a>
