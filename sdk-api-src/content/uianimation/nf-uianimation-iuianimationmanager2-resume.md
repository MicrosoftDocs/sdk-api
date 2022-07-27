---
UID: NF:uianimation.IUIAnimationManager2.Resume
title: IUIAnimationManager2::Resume (uianimation.h)
description: Resumes all animations. (IUIAnimationManager2.Resume)
helpviewer_keywords: ["IUIAnimationManager2 interface [Windows Animation]","Resume method","IUIAnimationManager2.Resume","IUIAnimationManager2::Resume","Resume","Resume method [Windows Animation]","Resume method [Windows Animation]","IUIAnimationManager2 interface","uianimation.iuianimationmanager2_resume","uianimation/IUIAnimationManager2::Resume"]
old-location: uianimation\iuianimationmanager2_resume.htm
tech.root: UIAnimation
ms.assetid: 943BCFBB-3E16-4CC8-BA9F-06D4C99B1DF0
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],Resume method, IUIAnimationManager2.Resume, IUIAnimationManager2::Resume, Resume, Resume method [Windows Animation], Resume method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_resume, uianimation/IUIAnimationManager2::Resume
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
 - IUIAnimationManager2::Resume
 - uianimation/IUIAnimationManager2::Resume
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
 - IUIAnimationManager2.Resume
---

# IUIAnimationManager2::Resume


## -description

Resumes all animations.



## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

When an animation manager is resumed, and at least one animation is currently scheduled or playing, its status is set to <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_manager_status">UI_ANIMATION_MANAGER_BUSY</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstatus">IUIAnimationManager::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-pause">IUIAnimationManager::Pause</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_manager_status">UI_ANIMATION_MANAGER_STATUS</a>
