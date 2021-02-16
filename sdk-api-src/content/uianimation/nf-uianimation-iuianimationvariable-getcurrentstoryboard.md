---
UID: NF:uianimation.IUIAnimationVariable.GetCurrentStoryboard
title: IUIAnimationVariable::GetCurrentStoryboard (uianimation.h)
description: Gets the storyboard that is currently animating the animation variable.
helpviewer_keywords: ["GetCurrentStoryboard","GetCurrentStoryboard method [Windows Animation]","GetCurrentStoryboard method [Windows Animation]","IUIAnimationVariable interface","IUIAnimationVariable interface [Windows Animation]","GetCurrentStoryboard method","IUIAnimationVariable.GetCurrentStoryboard","IUIAnimationVariable::GetCurrentStoryboard","uianimation.iuianimationvariable_getcurrentstoryboard","uianimation/IUIAnimationVariable::GetCurrentStoryboard"]
old-location: uianimation\iuianimationvariable_getcurrentstoryboard.htm
tech.root: UIAnimation
ms.assetid: 56042549-d6f6-4eed-8079-c1b14acbe160
ms.date: 12/05/2018
ms.keywords: GetCurrentStoryboard, GetCurrentStoryboard method [Windows Animation], GetCurrentStoryboard method [Windows Animation],IUIAnimationVariable interface, IUIAnimationVariable interface [Windows Animation],GetCurrentStoryboard method, IUIAnimationVariable.GetCurrentStoryboard, IUIAnimationVariable::GetCurrentStoryboard, uianimation.iuianimationvariable_getcurrentstoryboard, uianimation/IUIAnimationVariable::GetCurrentStoryboard
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
 - IUIAnimationVariable::GetCurrentStoryboard
 - uianimation/IUIAnimationVariable::GetCurrentStoryboard
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
 - IUIAnimationVariable.GetCurrentStoryboard
---

# IUIAnimationVariable::GetCurrentStoryboard


## -description

Gets the storyboard that is currently animating the animation variable.

## -parameters

### -param storyboard [out]

The current storyboard, or <b>NULL</b> if no storyboard is currently animating the animation variable.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">UIAnimation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>