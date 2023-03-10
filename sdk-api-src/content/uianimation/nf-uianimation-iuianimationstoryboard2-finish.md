---
UID: NF:uianimation.IUIAnimationStoryboard2.Finish
title: IUIAnimationStoryboard2::Finish (uianimation.h)
description: Finishes the storyboard within the specified time, compressing the storyboard if necessary. (IUIAnimationStoryboard2.Finish)
helpviewer_keywords: ["Finish","Finish method [Windows Animation]","Finish method [Windows Animation]","IUIAnimationStoryboard2 interface","IUIAnimationStoryboard2 interface [Windows Animation]","Finish method","IUIAnimationStoryboard2.Finish","IUIAnimationStoryboard2::Finish","uianimation.iuianimationstoryboard2_finish","uianimation/IUIAnimationStoryboard2::Finish"]
old-location: uianimation\iuianimationstoryboard2_finish.htm
tech.root: UIAnimation
ms.assetid: 632BC77D-F2C5-4D08-8E9C-0598617A1DA7
ms.date: 12/05/2018
ms.keywords: Finish, Finish method [Windows Animation], Finish method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],Finish method, IUIAnimationStoryboard2.Finish, IUIAnimationStoryboard2::Finish, uianimation.iuianimationstoryboard2_finish, uianimation/IUIAnimationStoryboard2::Finish
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
 - IUIAnimationStoryboard2::Finish
 - uianimation/IUIAnimationStoryboard2::Finish
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
 - IUIAnimationStoryboard2.Finish
---

# IUIAnimationStoryboard2::Finish


## -description

Finishes the storyboard within the specified time, compressing the storyboard if necessary.

## -parameters

### -param completionDeadline

The maximum amount of time that the storyboard can use to finish playing.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

This method has no effect on storyboard events. Events continue to be raised as expected while the storyboard plays.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-finishallstoryboards">IUIAnimationManager2::FinishAllStoryboards</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-abandon">IUIAnimationStoryboard2::Abandon</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-conclude">IUIAnimationStoryboard2::Conclude</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-schedule">IUIAnimationStoryboard2::Schedule</a>
