---
UID: NF:uianimation.IUIAnimationStoryboard.SetLongestAcceptableDelay
title: IUIAnimationStoryboard::SetLongestAcceptableDelay (uianimation.h)
description: Sets the longest acceptable delay before the scheduled storyboard begins. (IUIAnimationStoryboard.SetLongestAcceptableDelay)
helpviewer_keywords: ["IUIAnimationStoryboard interface [Windows Animation]","SetLongestAcceptableDelay method","IUIAnimationStoryboard.SetLongestAcceptableDelay","IUIAnimationStoryboard::SetLongestAcceptableDelay","SetLongestAcceptableDelay","SetLongestAcceptableDelay method [Windows Animation]","SetLongestAcceptableDelay method [Windows Animation]","IUIAnimationStoryboard interface","uianimation.iuianimationstoryboard_setlongestacceptabledelay","uianimation/IUIAnimationStoryboard::SetLongestAcceptableDelay"]
old-location: uianimation\iuianimationstoryboard_setlongestacceptabledelay.htm
tech.root: UIAnimation
ms.assetid: 5f87a4b1-8db9-42ba-963f-664db588c520
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard interface [Windows Animation],SetLongestAcceptableDelay method, IUIAnimationStoryboard.SetLongestAcceptableDelay, IUIAnimationStoryboard::SetLongestAcceptableDelay, SetLongestAcceptableDelay, SetLongestAcceptableDelay method [Windows Animation], SetLongestAcceptableDelay method [Windows Animation],IUIAnimationStoryboard interface, uianimation.iuianimationstoryboard_setlongestacceptabledelay, uianimation/IUIAnimationStoryboard::SetLongestAcceptableDelay
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
 - IUIAnimationStoryboard::SetLongestAcceptableDelay
 - uianimation/IUIAnimationStoryboard::SetLongestAcceptableDelay
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
 - IUIAnimationStoryboard.SetLongestAcceptableDelay
---

# IUIAnimationStoryboard::SetLongestAcceptableDelay


## -description

Sets the longest acceptable delay before the scheduled storyboard begins.

## -parameters

### -param delay [in]

The longest acceptable delay. This parameter can be a positive value, or <b>UI_ANIMATION_SECONDS_EVENTUALLY</b> (-1) to indicate that any finite delay is acceptable.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

For a storyboard to be successfully scheduled, it must begin before the longest acceptable delay has elapsed. This delay is determined in the following order: the delay value set by calling this method, the delay value set by calling the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setdefaultlongestacceptabledelay">IUIAnimationManager::SetDefaultLongestAcceptableDelay</a> method, or 0.0 if neither of these methods has been called.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-setdefaultlongestacceptabledelay">IUIAnimationManager::SetDefaultLongestAcceptableDelay</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>
