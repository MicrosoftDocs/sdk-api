---
UID: NF:uianimation.IUIAnimationStoryboard2.SetLongestAcceptableDelay
title: IUIAnimationStoryboard2::SetLongestAcceptableDelay (uianimation.h)
description: Sets the longest acceptable delay before the scheduled storyboard begins. (IUIAnimationStoryboard2.SetLongestAcceptableDelay)
helpviewer_keywords: ["IUIAnimationStoryboard2 interface [Windows Animation]","SetLongestAcceptableDelay method","IUIAnimationStoryboard2.SetLongestAcceptableDelay","IUIAnimationStoryboard2::SetLongestAcceptableDelay","SetLongestAcceptableDelay","SetLongestAcceptableDelay method [Windows Animation]","SetLongestAcceptableDelay method [Windows Animation]","IUIAnimationStoryboard2 interface","uianimation.iuianimationstoryboard2_setlongestacceptabledelay","uianimation/IUIAnimationStoryboard2::SetLongestAcceptableDelay"]
old-location: uianimation\iuianimationstoryboard2_setlongestacceptabledelay.htm
tech.root: UIAnimation
ms.assetid: D23F4833-413C-470B-8572-2DCB051576A3
ms.date: 12/05/2018
ms.keywords: IUIAnimationStoryboard2 interface [Windows Animation],SetLongestAcceptableDelay method, IUIAnimationStoryboard2.SetLongestAcceptableDelay, IUIAnimationStoryboard2::SetLongestAcceptableDelay, SetLongestAcceptableDelay, SetLongestAcceptableDelay method [Windows Animation], SetLongestAcceptableDelay method [Windows Animation],IUIAnimationStoryboard2 interface, uianimation.iuianimationstoryboard2_setlongestacceptabledelay, uianimation/IUIAnimationStoryboard2::SetLongestAcceptableDelay
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
 - IUIAnimationStoryboard2::SetLongestAcceptableDelay
 - uianimation/IUIAnimationStoryboard2::SetLongestAcceptableDelay
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
 - IUIAnimationStoryboard2.SetLongestAcceptableDelay
---

# IUIAnimationStoryboard2::SetLongestAcceptableDelay


## -description

Sets the longest acceptable delay before the scheduled storyboard begins.

## -parameters

### -param delay [in]

The longest acceptable delay. This parameter can be a positive value, or <a href="/windows/desktop/UIAnimation/ui-animation-seconds-eventually">UI_ANIMATION_SECONDS_EVENTUALLY</a> (-1) to indicate that any finite delay is acceptable.

## -returns

Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

For Windows Animation to schedule a storyboard successfully, the storyboard must begin before the longest acceptable delay has elapsed. Windows Animation determines this delay in the following order: the delay value set by calling this method, the delay value set by calling the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setdefaultlongestacceptabledelay">IUIAnimationManager2::SetDefaultLongestAcceptableDelay</a> method, or 0.0 if neither of these methods has been called.

 Use <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-setskipduration">IUIAnimationStoryboard2::SetSkipDuration</a> to start a storyboard animation at a specified offset instead of delaying the start of a storyboard.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard2">IUIAnimationStoryboard2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationstoryboard2-setskipduration">SetSkipDuration</a>
