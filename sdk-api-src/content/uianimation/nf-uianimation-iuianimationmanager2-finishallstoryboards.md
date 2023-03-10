---
UID: NF:uianimation.IUIAnimationManager2.FinishAllStoryboards
title: IUIAnimationManager2::FinishAllStoryboards (uianimation.h)
description: Finishes all active storyboards within the specified time interval. (IUIAnimationManager2.FinishAllStoryboards)
helpviewer_keywords: ["FinishAllStoryboards","FinishAllStoryboards method [Windows Animation]","FinishAllStoryboards method [Windows Animation]","IUIAnimationManager2 interface","IUIAnimationManager2 interface [Windows Animation]","FinishAllStoryboards method","IUIAnimationManager2.FinishAllStoryboards","IUIAnimationManager2::FinishAllStoryboards","uianimation.iuianimationmanager2_finishallstoryboards","uianimation/IUIAnimationManager2::FinishAllStoryboards"]
old-location: uianimation\iuianimationmanager2_finishallstoryboards.htm
tech.root: UIAnimation
ms.assetid: 830A5D30-68FF-4226-AC7C-7B1C5F7BA367
ms.date: 12/05/2018
ms.keywords: FinishAllStoryboards, FinishAllStoryboards method [Windows Animation], FinishAllStoryboards method [Windows Animation],IUIAnimationManager2 interface, IUIAnimationManager2 interface [Windows Animation],FinishAllStoryboards method, IUIAnimationManager2.FinishAllStoryboards, IUIAnimationManager2::FinishAllStoryboards, uianimation.iuianimationmanager2_finishallstoryboards, uianimation/IUIAnimationManager2::FinishAllStoryboards
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
 - IUIAnimationManager2::FinishAllStoryboards
 - uianimation/IUIAnimationManager2::FinishAllStoryboards
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
 - IUIAnimationManager2.FinishAllStoryboards
---

# IUIAnimationManager2::FinishAllStoryboards


## -description

Finishes all active storyboards within the specified time interval.

## -parameters

### -param completionDeadline [in]

The maximum time interval during which all storyboards must be finished.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Calling the <b>FinishAllStoryboards</b> method ensures that all active storyboards finish within the specified completion deadline. If a storyboard is scheduled to play past the deadline, it is compressed.

A storyboard is considered active if a call to the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a> method returns <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_PLAYING</a> 
         or <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_SCHEDULED</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-finish">IUIAnimationStoryboard::Finish</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
