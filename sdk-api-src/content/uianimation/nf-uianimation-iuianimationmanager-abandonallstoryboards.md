---
UID: NF:uianimation.IUIAnimationManager.AbandonAllStoryboards
title: IUIAnimationManager::AbandonAllStoryboards (uianimation.h)
description: Abandons all active storyboards. (IUIAnimationManager.AbandonAllStoryboards)
helpviewer_keywords: ["AbandonAllStoryboards","AbandonAllStoryboards method [Windows Animation]","AbandonAllStoryboards method [Windows Animation]","IUIAnimationManager interface","IUIAnimationManager interface [Windows Animation]","AbandonAllStoryboards method","IUIAnimationManager.AbandonAllStoryboards","IUIAnimationManager::AbandonAllStoryboards","uianimation.iuianimationmanager_abandonallstoryboards","uianimation/IUIAnimationManager::AbandonAllStoryboards"]
old-location: uianimation\iuianimationmanager_abandonallstoryboards.htm
tech.root: UIAnimation
ms.assetid: cecb0026-ed6f-48b8-9381-d020a36e7e87
ms.date: 12/05/2018
ms.keywords: AbandonAllStoryboards, AbandonAllStoryboards method [Windows Animation], AbandonAllStoryboards method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],AbandonAllStoryboards method, IUIAnimationManager.AbandonAllStoryboards, IUIAnimationManager::AbandonAllStoryboards, uianimation.iuianimationmanager_abandonallstoryboards, uianimation/IUIAnimationManager::AbandonAllStoryboards
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
 - IUIAnimationManager::AbandonAllStoryboards
 - uianimation/IUIAnimationManager::AbandonAllStoryboards
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
 - IUIAnimationManager.AbandonAllStoryboards
---

# IUIAnimationManager::AbandonAllStoryboards


## -description

Abandons all active storyboards.



## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Calling this method is equivalent to calling the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-abandon">IUIAnimationStoryboard::Abandon</a> method for each active storyboard.
         
A storyboard is considered active if its status is <b>UI_ANIMATION_STORYBOARD_PLAYING</b> or <b>UI_ANIMATION_STORYBOARD_SCHEDULED</b>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-abandon">IUIAnimationStoryboard::Abandon</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
