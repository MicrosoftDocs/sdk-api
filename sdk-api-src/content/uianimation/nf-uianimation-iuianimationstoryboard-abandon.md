---
UID: NF:uianimation.IUIAnimationStoryboard.Abandon
title: IUIAnimationStoryboard::Abandon (uianimation.h)
description: Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule. (IUIAnimationStoryboard.Abandon)
helpviewer_keywords: ["Abandon","Abandon method [Windows Animation]","Abandon method [Windows Animation]","IUIAnimationStoryboard interface","IUIAnimationStoryboard interface [Windows Animation]","Abandon method","IUIAnimationStoryboard.Abandon","IUIAnimationStoryboard::Abandon","uianimation.iuianimationstoryboard_abandon","uianimation/IUIAnimationStoryboard::Abandon"]
old-location: uianimation\iuianimationstoryboard_abandon.htm
tech.root: UIAnimation
ms.assetid: 2350dbd0-3a67-4832-94dd-56adce80a387
ms.date: 12/05/2018
ms.keywords: Abandon, Abandon method [Windows Animation], Abandon method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],Abandon method, IUIAnimationStoryboard.Abandon, IUIAnimationStoryboard::Abandon, uianimation.iuianimationstoryboard_abandon, uianimation/IUIAnimationStoryboard::Abandon
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
 - IUIAnimationStoryboard::Abandon
 - uianimation/IUIAnimationStoryboard::Abandon
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
 - IUIAnimationStoryboard.Abandon
---

# IUIAnimationStoryboard::Abandon


## -description

Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.



## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method can be called before or after the storyboard starts playing.

This method does not trigger any storyboard events.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-abandonallstoryboards">IUIAnimationManager::AbandonAllStoryboards</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-conclude">IUIAnimationStoryboard::Conclude</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-finish">IUIAnimationStoryboard::Finish</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-schedule">IUIAnimationStoryboard::Schedule</a>
