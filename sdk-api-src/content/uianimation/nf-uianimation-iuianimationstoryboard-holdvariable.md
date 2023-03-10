---
UID: NF:uianimation.IUIAnimationStoryboard.HoldVariable
title: IUIAnimationStoryboard::HoldVariable (uianimation.h)
description: Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends. (IUIAnimationStoryboard.HoldVariable)
helpviewer_keywords: ["HoldVariable","HoldVariable method [Windows Animation]","HoldVariable method [Windows Animation]","IUIAnimationStoryboard interface","IUIAnimationStoryboard interface [Windows Animation]","HoldVariable method","IUIAnimationStoryboard.HoldVariable","IUIAnimationStoryboard::HoldVariable","uianimation.iuianimationstoryboard_holdvariable","uianimation/IUIAnimationStoryboard::HoldVariable"]
old-location: uianimation\iuianimationstoryboard_holdvariable.htm
tech.root: UIAnimation
ms.assetid: ac5ee9c0-cecb-41f1-b8d3-6f779dfafef7
ms.date: 12/05/2018
ms.keywords: HoldVariable, HoldVariable method [Windows Animation], HoldVariable method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],HoldVariable method, IUIAnimationStoryboard.HoldVariable, IUIAnimationStoryboard::HoldVariable, uianimation.iuianimationstoryboard_holdvariable, uianimation/IUIAnimationStoryboard::HoldVariable
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
 - IUIAnimationStoryboard::HoldVariable
 - uianimation/IUIAnimationStoryboard::HoldVariable
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
 - IUIAnimationStoryboard.HoldVariable
---

# IUIAnimationStoryboard::HoldVariable


## -description

Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.

## -parameters

### -param variable [in]

The animation variable.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

When a storyboard is playing, it has exclusive access to any variables it animates unless the storyboard is trimmed by a higher priority storyboard. Typically, this exclusive access is released  when the last transition in the storyboard for that variable finishes playing. Applications can call this method to maintain exclusive access to the animation variable and hold the variable, at the final value of the last transition, until the end of the storyboard.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationstoryboard">IUIAnimationStoryboard</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>
