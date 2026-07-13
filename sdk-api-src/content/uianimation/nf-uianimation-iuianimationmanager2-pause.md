---
UID: NF:uianimation.IUIAnimationManager2.Pause
title: IUIAnimationManager2::Pause (uianimation.h)
description: Pauses all animations. (IUIAnimationManager2.Pause)
helpviewer_keywords: ["IUIAnimationManager2 interface [Windows Animation]","Pause method","IUIAnimationManager2.Pause","IUIAnimationManager2::Pause","Pause","Pause method [Windows Animation]","Pause method [Windows Animation]","IUIAnimationManager2 interface","uianimation.iuianimationmanager2_pause","uianimation/IUIAnimationManager2::Pause"]
old-location: uianimation\iuianimationmanager2_pause.htm
tech.root: UIAnimation
ms.assetid: AA8EEFD5-A386-4DF1-BCBE-12A92D235E98
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],Pause method, IUIAnimationManager2.Pause, IUIAnimationManager2::Pause, Pause, Pause method [Windows Animation], Pause method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_pause, uianimation/IUIAnimationManager2::Pause
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
 - IUIAnimationManager2::Pause
 - uianimation/IUIAnimationManager2::Pause
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
 - IUIAnimationManager2.Pause
---

# IUIAnimationManager2::Pause


## -description

Pauses all animations.



## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

When an animation manager is paused, its status is set to <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_manager_status">UI_ANIMATION_MANAGER_IDLE</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstatus">IUIAnimationManager::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-resume">IUIAnimationManager::Resume</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_manager_status">UI_ANIMATION_MANAGER_STATUS</a>
