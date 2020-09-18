---
UID: NF:uianimation.IUIAnimationVariable2.GetCurrentStoryboard
title: IUIAnimationVariable2::GetCurrentStoryboard (uianimation.h)
description: Gets the active storyboard for the animation variable.
helpviewer_keywords: ["GetCurrentStoryboard","GetCurrentStoryboard method [Windows Animation]","GetCurrentStoryboard method [Windows Animation]","IUIAnimationVariable2 interface","IUIAnimationVariable2 interface [Windows Animation]","GetCurrentStoryboard method","IUIAnimationVariable2.GetCurrentStoryboard","IUIAnimationVariable2::GetCurrentStoryboard","uianimation.iuianimationvariable2_getcurrentstoryboard","uianimation/IUIAnimationVariable2::GetCurrentStoryboard"]
old-location: uianimation\iuianimationvariable2_getcurrentstoryboard.htm
tech.root: UIAnimation
ms.assetid: 7A9B4A84-94E4-4B6C-B2FF-0A0A70397D21
ms.date: 12/05/2018
ms.keywords: GetCurrentStoryboard, GetCurrentStoryboard method [Windows Animation], GetCurrentStoryboard method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetCurrentStoryboard method, IUIAnimationVariable2.GetCurrentStoryboard, IUIAnimationVariable2::GetCurrentStoryboard, uianimation.iuianimationvariable2_getcurrentstoryboard, uianimation/IUIAnimationVariable2::GetCurrentStoryboard
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
 - IUIAnimationVariable2::GetCurrentStoryboard
 - uianimation/IUIAnimationVariable2::GetCurrentStoryboard
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
 - IUIAnimationVariable2.GetCurrentStoryboard
---

# IUIAnimationVariable2::GetCurrentStoryboard


## -description

Gets the active storyboard for the animation variable.

## -parameters

### -param storyboard [out]

The active storyboard, or NULL if the animation variable is not being animated.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>