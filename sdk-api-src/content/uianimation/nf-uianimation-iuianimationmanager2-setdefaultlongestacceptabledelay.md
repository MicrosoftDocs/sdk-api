---
UID: NF:uianimation.IUIAnimationManager2.SetDefaultLongestAcceptableDelay
title: IUIAnimationManager2::SetDefaultLongestAcceptableDelay (uianimation.h)
description: Sets the default acceptable animation delay. This is the length of time that may pass before storyboards begin. (IUIAnimationManager2.SetDefaultLongestAcceptableDelay)
helpviewer_keywords: ["IUIAnimationManager2 interface [Windows Animation]","SetDefaultLongestAcceptableDelay method","IUIAnimationManager2.SetDefaultLongestAcceptableDelay","IUIAnimationManager2::SetDefaultLongestAcceptableDelay","SetDefaultLongestAcceptableDelay","SetDefaultLongestAcceptableDelay method [Windows Animation]","SetDefaultLongestAcceptableDelay method [Windows Animation]","IUIAnimationManager2 interface","uianimation.iuianimationmanager2_setdefaultlongestacceptabledelay","uianimation/IUIAnimationManager2::SetDefaultLongestAcceptableDelay"]
old-location: uianimation\iuianimationmanager2_setdefaultlongestacceptabledelay.htm
tech.root: UIAnimation
ms.assetid: CB00C22B-9837-43AD-9E04-30182B7386E9
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],SetDefaultLongestAcceptableDelay method, IUIAnimationManager2.SetDefaultLongestAcceptableDelay, IUIAnimationManager2::SetDefaultLongestAcceptableDelay, SetDefaultLongestAcceptableDelay, SetDefaultLongestAcceptableDelay method [Windows Animation], SetDefaultLongestAcceptableDelay method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_setdefaultlongestacceptabledelay, uianimation/IUIAnimationManager2::SetDefaultLongestAcceptableDelay
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
 - IUIAnimationManager2::SetDefaultLongestAcceptableDelay
 - uianimation/IUIAnimationManager2::SetDefaultLongestAcceptableDelay
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
 - IUIAnimationManager2.SetDefaultLongestAcceptableDelay
---

# IUIAnimationManager2::SetDefaultLongestAcceptableDelay


## -description

Sets the default acceptable animation delay. This is the length of time that may pass before storyboards begin.

## -parameters

### -param delay [in]

The default delay. This parameter can be a positive value, or <a href="/windows/desktop/UIAnimation/ui-animation-seconds-eventually">UI_ANIMATION_SECONDS_EVENTUALLY</a> (-1) to indicate that any finite delay is acceptable.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

For Windows Animation to schedule a storyboard successfully, the storyboard must begin before the longest acceptable delay has elapsed. Windows Animation determines this delay in the following order: the delay value set by calling <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay">IUIAnimationStoryboard::SetLongestAcceptableDelay</a> for this specific storyboard, the delay value set by calling this method, or 0.0 if neither method has been called.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay">IUIAnimationStoryboard::SetLongestAcceptableDelay</a>
