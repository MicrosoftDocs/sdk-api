---
UID: NF:uianimation.IUIAnimationManager2.AbandonAllStoryboards
title: IUIAnimationManager2::AbandonAllStoryboards (uianimation.h)
description: Abandons all active storyboards. (IUIAnimationManager2.AbandonAllStoryboards)
helpviewer_keywords: ["AbandonAllStoryboards","AbandonAllStoryboards method [Windows Animation]","AbandonAllStoryboards method [Windows Animation]","IUIAnimationManager2 interface","IUIAnimationManager2 interface [Windows Animation]","AbandonAllStoryboards method","IUIAnimationManager2.AbandonAllStoryboards","IUIAnimationManager2::AbandonAllStoryboards","uianimation.iuianimationmanager2_abandonallstoryboards","uianimation/IUIAnimationManager2::AbandonAllStoryboards"]
old-location: uianimation\iuianimationmanager2_abandonallstoryboards.htm
tech.root: UIAnimation
ms.assetid: E8DC71C0-CA68-4FD8-81CE-68450BF4EBA7
ms.date: 12/05/2018
ms.keywords: AbandonAllStoryboards, AbandonAllStoryboards method [Windows Animation], AbandonAllStoryboards method [Windows Animation],IUIAnimationManager2 interface, IUIAnimationManager2 interface [Windows Animation],AbandonAllStoryboards method, IUIAnimationManager2.AbandonAllStoryboards, IUIAnimationManager2::AbandonAllStoryboards, uianimation.iuianimationmanager2_abandonallstoryboards, uianimation/IUIAnimationManager2::AbandonAllStoryboards
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
 - IUIAnimationManager2::AbandonAllStoryboards
 - uianimation/IUIAnimationManager2::AbandonAllStoryboards
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
 - IUIAnimationManager2.AbandonAllStoryboards
---

# IUIAnimationManager2::AbandonAllStoryboards


## -description

Abandons all active storyboards.



## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Calling this method is equivalent to calling the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-abandon">IUIAnimationStoryboard::Abandon</a> method for each active storyboard.
         
         

A storyboard is considered active if a call to the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a> method returns <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_PLAYING</a> 
         or <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_SCHEDULED</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-abandon">IUIAnimationStoryboard::Abandon</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-getstatus">IUIAnimationStoryboard::GetStatus</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status">UI_ANIMATION_STORYBOARD_STATUS</a>
