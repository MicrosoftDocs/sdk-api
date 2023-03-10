---
UID: NF:uianimation.IUIAnimationTransition2.GetDuration
title: IUIAnimationTransition2::GetDuration (uianimation.h)
description: Gets the duration of the transition. (IUIAnimationTransition2.GetDuration)
helpviewer_keywords: ["GetDuration","GetDuration method [Windows Animation]","GetDuration method [Windows Animation]","IUIAnimationTransition2 interface","IUIAnimationTransition2 interface [Windows Animation]","GetDuration method","IUIAnimationTransition2.GetDuration","IUIAnimationTransition2::GetDuration","uianimation.iuianimationtransition2_getduration","uianimation/IUIAnimationTransition2::GetDuration"]
old-location: uianimation\iuianimationtransition2_getduration.htm
tech.root: UIAnimation
ms.assetid: 07B5C7D7-80B1-4458-93A7-39F61121B618
ms.date: 12/05/2018
ms.keywords: GetDuration, GetDuration method [Windows Animation], GetDuration method [Windows Animation],IUIAnimationTransition2 interface, IUIAnimationTransition2 interface [Windows Animation],GetDuration method, IUIAnimationTransition2.GetDuration, IUIAnimationTransition2::GetDuration, uianimation.iuianimationtransition2_getduration, uianimation/IUIAnimationTransition2::GetDuration
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
 - IUIAnimationTransition2::GetDuration
 - uianimation/IUIAnimationTransition2::GetDuration
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
 - IUIAnimationTransition2.GetDuration
---

# IUIAnimationTransition2::GetDuration


## -description

Gets the duration of the transition.

## -parameters

### -param duration [out]

The duration of the transition, in seconds.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

An application should typically call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-isdurationknown">IsDurationKnown</a> method before calling this method. 

This method should not be called when the storyboard to which the transition has been added is scheduled or playing.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>
