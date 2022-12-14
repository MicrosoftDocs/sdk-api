---
UID: NF:uianimation.IUIAnimationStoryboard2.Abandon
title: IUIAnimationStoryboard2::Abandon (uianimation.h)
description: Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule. (IUIAnimationStoryboard2.Abandon)
helpviewer_keywords: ["Abandon","Abandon method [Windows Animation]","Abandon method [Windows Animation]","IUIAnimationStoryboard2 interface","IUIAnimationStoryboard2 interface [Windows Animation]","Abandon method","IUIAnimationStoryboard2.Abandon","IUIAnimationStoryboard2::Abandon","uianimation.iuianimationstoryboard2_abandon","uianimation/IUIAnimationStoryboard2::Abandon"]
old-location: uianimation\iuianimationstoryboard2_abandon.htm
tech.root: UIAnimation
ms.assetid: ABB7184F-A703-45E3-96D8-E3062EEB9565
ms.date: 12/05/2018
ms.keywords: Abandon, Abandon method [Windows Animation], Abandon method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],Abandon method, IUIAnimationStoryboard2.Abandon, IUIAnimationStoryboard2::Abandon, uianimation.iuianimationstoryboard2_abandon, uianimation/IUIAnimationStoryboard2::Abandon
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
 - IUIAnimationStoryboard2::Abandon
 - uianimation/IUIAnimationStoryboard2::Abandon
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
 - IUIAnimationStoryboard2.Abandon
---

# IUIAnimationStoryboard2::Abandon


## -description

Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.



## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method can be called before or after the storyboard starts playing.

This method does not trigger any storyboard events.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-abandonallstoryboards">IUIAnimationManager2::AbandonAllStoryboards</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-conclude">IUIAnimationStoryboard2::Conclude</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-finish">IUIAnimationStoryboard2::Finish</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-schedule">IUIAnimationStoryboard2::Schedule</a>
