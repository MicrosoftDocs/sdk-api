---
UID: NF:uianimation.IUIAnimationManager.Resume
title: IUIAnimationManager::Resume (uianimation.h)
description: Resumes all animations. (IUIAnimationManager.Resume)
helpviewer_keywords: ["IUIAnimationManager interface [Windows Animation]","Resume method","IUIAnimationManager.Resume","IUIAnimationManager::Resume","Resume","Resume method [Windows Animation]","Resume method [Windows Animation]","IUIAnimationManager interface","uianimation.iuianimationmanager_resume","uianimation/IUIAnimationManager::Resume"]
old-location: uianimation\iuianimationmanager_resume.htm
tech.root: UIAnimation
ms.assetid: f29a9337-0ed0-46f8-ab77-8f82ab39d8df
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],Resume method, IUIAnimationManager.Resume, IUIAnimationManager::Resume, Resume, Resume method [Windows Animation], Resume method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_resume, uianimation/IUIAnimationManager::Resume
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
 - IUIAnimationManager::Resume
 - uianimation/IUIAnimationManager::Resume
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
 - IUIAnimationManager.Resume
---

# IUIAnimationManager::Resume


## -description

Resumes all animations.



## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

When an animation manager is resumed, and at least one animation is currently scheduled or playing, its status is set to <b>UI_ANIMATION_MANAGER_BUSY</b>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstatus">IUIAnimationManager::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-pause">IUIAnimationManager::Pause</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_manager_status">UI_ANIMATION_MANAGER_STATUS</a>
