---
UID: NF:uianimation.IUIAnimationManager.SetDefaultLongestAcceptableDelay
title: IUIAnimationManager::SetDefaultLongestAcceptableDelay (uianimation.h)
description: Sets the default acceptable animation delay. This is the length of time that may pass before storyboards begin. (IUIAnimationManager.SetDefaultLongestAcceptableDelay)
helpviewer_keywords: ["IUIAnimationManager interface [Windows Animation]","SetDefaultLongestAcceptableDelay method","IUIAnimationManager.SetDefaultLongestAcceptableDelay","IUIAnimationManager::SetDefaultLongestAcceptableDelay","SetDefaultLongestAcceptableDelay","SetDefaultLongestAcceptableDelay method [Windows Animation]","SetDefaultLongestAcceptableDelay method [Windows Animation]","IUIAnimationManager interface","uianimation.iuianimationmanager_setdefaultlongestacceptabledelay","uianimation/IUIAnimationManager::SetDefaultLongestAcceptableDelay"]
old-location: uianimation\iuianimationmanager_setdefaultlongestacceptabledelay.htm
tech.root: UIAnimation
ms.assetid: 27182009-1614-41a0-9b55-7c1dcb494883
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],SetDefaultLongestAcceptableDelay method, IUIAnimationManager.SetDefaultLongestAcceptableDelay, IUIAnimationManager::SetDefaultLongestAcceptableDelay, SetDefaultLongestAcceptableDelay, SetDefaultLongestAcceptableDelay method [Windows Animation], SetDefaultLongestAcceptableDelay method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_setdefaultlongestacceptabledelay, uianimation/IUIAnimationManager::SetDefaultLongestAcceptableDelay
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
 - IUIAnimationManager::SetDefaultLongestAcceptableDelay
 - uianimation/IUIAnimationManager::SetDefaultLongestAcceptableDelay
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
 - IUIAnimationManager.SetDefaultLongestAcceptableDelay
---

# IUIAnimationManager::SetDefaultLongestAcceptableDelay


## -description

Sets the default acceptable animation delay. This is the length of time that may pass before storyboards begin.

## -parameters

### -param delay [in]

The default delay. This parameter can be a positive value, or <b>UI_ANIMATION_SECONDS_EVENTUALLY</b> (-1) to indicate that any finite delay is acceptable.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.            
            See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

For a storyboard to be successfully scheduled, it must begin before the longest acceptable delay has elapsed. This delay is determined in the following order: the delay value set by calling <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay">IUIAnimationStoryboard::SetLongestAcceptableDelay</a> for this specific storyboard, the delay value set by calling this method, or 0.0 if neither method has been called.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay">IUIAnimationStoryboard::SetLongestAcceptableDelay</a>
