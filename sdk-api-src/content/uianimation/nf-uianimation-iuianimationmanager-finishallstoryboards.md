---
UID: NF:uianimation.IUIAnimationManager.FinishAllStoryboards
title: IUIAnimationManager::FinishAllStoryboards (uianimation.h)
description: Finishes all active storyboards within the specified time interval. (IUIAnimationManager.FinishAllStoryboards)
helpviewer_keywords: ["FinishAllStoryboards","FinishAllStoryboards method [Windows Animation]","FinishAllStoryboards method [Windows Animation]","IUIAnimationManager interface","IUIAnimationManager interface [Windows Animation]","FinishAllStoryboards method","IUIAnimationManager.FinishAllStoryboards","IUIAnimationManager::FinishAllStoryboards","uianimation.iuianimationmanager_finishallstoryboards","uianimation/IUIAnimationManager::FinishAllStoryboards"]
old-location: uianimation\iuianimationmanager_finishallstoryboards.htm
tech.root: UIAnimation
ms.assetid: db5ba70c-3904-4053-881a-b1412beb35f3
ms.date: 12/05/2018
ms.keywords: FinishAllStoryboards, FinishAllStoryboards method [Windows Animation], FinishAllStoryboards method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],FinishAllStoryboards method, IUIAnimationManager.FinishAllStoryboards, IUIAnimationManager::FinishAllStoryboards, uianimation.iuianimationmanager_finishallstoryboards, uianimation/IUIAnimationManager::FinishAllStoryboards
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
 - IUIAnimationManager::FinishAllStoryboards
 - uianimation/IUIAnimationManager::FinishAllStoryboards
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
 - IUIAnimationManager.FinishAllStoryboards
---

# IUIAnimationManager::FinishAllStoryboards


## -description

Finishes all active storyboards within the specified time interval.

## -parameters

### -param completionDeadline [in]

The maximum time interval during which all storyboards must be finished.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Calling <b>FinishAllStoryboards</b> ensures that all active storyboards finish within the specified completion deadline. If a storyboard is scheduled to play past the deadline, it is compressed.
         
A storyboard is considered active if its status is <b>UI_ANIMATION_STORYBOARD_PLAYING</b> or <b>UI_ANIMATION_STORYBOARD_SCHEDULED</b>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-finish">IUIAnimationStoryboard::Finish</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
